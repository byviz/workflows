# 🎓 Workflows Básicos

Workflows fundamentales para aprender la sintaxis y conceptos core de Elastic Workflows.

## 📚 Contenido

| Workflow | Descripción | Trigger | Dificultad |
|----------|-------------|---------|------------|
| `01-manual-trigger.yaml` | Ejecución manual on-demand | Manual | ⭐ |
| `02-scheduled-basic.yaml` | Programación con cron | Scheduled | ⭐ |
| `03-alert-trigger.yaml` | Disparo desde alertas | Alert | ⭐⭐ |
| `04-inputs-example.yaml` | Uso de inputs dinámicos | Manual | ⭐ |
| `05-constants-example.yaml` | Constantes reutilizables | Manual | ⭐ |
| `06-templating-liquid.yaml` | Templating con Liquid | Manual | ⭐⭐ |

## 🎯 Conceptos que aprenderás

### 1. Triggers (Disparadores)
- **Manual**: Ejecución on-demand para testing
- **Scheduled**: Programación automática con cron
- **Alert**: Respuesta automática a alertas

### 2. Steps (Pasos)
- Búsquedas en Elasticsearch
- Operaciones de control de flujo
- Salida a consola para debugging

### 3. Inputs (Entradas)
- Parámetros configurables
- Valores por defecto
- Validaciones

### 4. Constants (Constantes)
- Valores reutilizables
- Configuración centralizada

### 5. Templating con Liquid
- Acceso a variables
- Interpolación de datos
- Navegación de objetos

## 🚀 Cómo usarlos

1. **Empieza por el manual trigger** (`01-manual-trigger.yaml`)
2. **Prueba cada ejemplo** en Kibana
3. **Modifica valores** para entender el comportamiento
4. **Revisa los outputs** en el historial de ejecuciones
5. **Avanza gradualmente** a workflows más complejos

## 💡 Tips

- Usa `type: console` para debugging
- El historial de ejecuciones muestra cada step
- Los manual triggers son perfectos para testing
- Revisa la sintaxis Liquid para templating avanzado

## 📖 Referencias

- [Documentación Oficial - Triggers](https://www.elastic.co/docs/explore-analyze/workflows/triggers)
- [Documentación Oficial - Steps](https://www.elastic.co/docs/explore-analyze/workflows/steps)
- [Guía Liquid Templating](https://byviz.ai/workflows#templating)

---

**Siguiente paso:** Una vez domines estos básicos, continúa con [02-busqueda-agregacion](../02-busqueda-agregacion/)

