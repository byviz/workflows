# 🧪 Tests de Sintaxis de Sort

## Objetivo

Estos workflows de test determinan cuál es la sintaxis correcta de `sort` en Elastic Workflows 9.3.

## Error detectado

```
No mapping found for [@timestamp:desc] in order to sort on
```

Esto indica que la sintaxis `"@timestamp:desc"` no es la correcta.

## 📋 Archivos de test

He creado 4 workflows para probar diferentes sintaxis:

### 1️⃣ `99-test-sort-option-1.yaml` - String con dos puntos
```yaml
sort:
  - "@timestamp:desc"
```

### 2️⃣ `99-test-sort-option-2.yaml` - Objeto inline
```yaml
sort:
  - "@timestamp": desc
```

### 3️⃣ `99-test-sort-option-3.yaml` - Objeto completo
```yaml
sort:
  - "@timestamp":
      order: desc
```

### 4️⃣ `99-test-sort-option-4.yaml` - Sin sort (control)
```yaml
# Sin parámetro sort
# Para verificar que la búsqueda base funciona
```

## 🚀 Cómo ejecutar los tests

### Opción A: En Kibana UI (Recomendado)

1. Ve a **Kibana → Stack Management → Workflows**
2. Crea un nuevo workflow
3. Copia el contenido de cada archivo yaml de test
4. Guarda y ejecuta manualmente
5. Revisa los logs de la consola

### Opción B: Si hay indice con pocos datos

Si el índice `logs-*` no tiene datos o tiene pocos en la última hora, prueba con:

- Cambia `index: "logs-*"` por `.monitoring-*` o el índice que sepas que tiene datos
- Ajusta el time range de `now-1h` a `now-24h` si es necesario

## 🎯 Orden de ejecución sugerido

1. **Primero:** Ejecuta `option-4` (sin sort) para verificar que la búsqueda base funciona
2. **Segundo:** Ejecuta `option-3` (objeto completo) - la sintaxis más estándar de Elasticsearch
3. **Tercero:** Ejecuta `option-2` (objeto inline) - sintaxis abreviada
4. **Cuarto:** Ejecuta `option-1` (string) - la que ya sabemos que falla

## ✅ Identificar cuál funciona

- Si el workflow **se ejecuta completo** y ves el mensaje final → ✅ **FUNCIONA**
- Si el workflow **falla** en el step de búsqueda → ❌ **NO FUNCIONA**

Una vez identificada la sintaxis correcta, actualizaremos todos los workflows del repositorio.

## 🗑️ Limpieza

Una vez identificada la sintaxis correcta, estos archivos de test pueden eliminarse:

- `99-test-sort-option-1.yaml`
- `99-test-sort-option-2.yaml`
- `99-test-sort-option-3.yaml`
- `99-test-sort-option-4.yaml`
- `README-TEST-SORT.md` (este archivo)

