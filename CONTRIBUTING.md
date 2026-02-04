# 🤝 Guía de Contribución

¡Gracias por tu interés en contribuir a este repositorio de Elastic Workflows!

## 🎯 Formas de Contribuir

### 1. 🐛 Reportar Issues
- Usa el [issue tracker](https://github.com/byviz/workflows/issues)
- Describe el problema claramente
- Incluye versión de Elastic
- Proporciona pasos para reproducir

### 2. 💡 Proponer Nuevos Workflows
- Abre un issue describiendo el caso de uso
- Explica qué problema resuelve
- Si es posible, incluye un borrador en YAML

### 3. ✏️ Mejorar Documentación
- Correcciones de typos
- Clarificaciones
- Traducciones
- Ejemplos adicionales

### 4. 🔧 Enviar Workflows
Sigue estas pautas:

#### Estructura del Workflow

```yaml
# ═══════════════════════════════════════════════════════════════
# WORKFLOW: [Nombre descriptivo]
# ═══════════════════════════════════════════════════════════════
# Descripción: [Qué hace este workflow]
# Caso de uso: [Cuándo usarlo]
# Requisitos: Elastic 9.3+, [índices], [connectors]
# Autor: [Tu nombre]
# ═══════════════════════════════════════════════════════════════

name: nombre-descriptivo
description: |
  Descripción detallada de qué hace
enabled: true
tags: ["categoria", "subcategoria"]

# ... resto del workflow
```

#### Checklist antes de enviar

- [ ] Workflow testeado en Elastic 9.3+
- [ ] Documentación clara en español
- [ ] Sin credenciales hardcoded
- [ ] Variables de ejemplo genéricas
- [ ] Comentarios explicativos
- [ ] README actualizado en la carpeta correspondiente

#### Proceso de Pull Request

1. **Fork** el repositorio
2. **Crea una rama** descriptiva: `git checkout -b feature/mi-workflow`
3. **Añade tu workflow** en la carpeta apropiada
4. **Actualiza el README** de esa carpeta
5. **Commit** con mensaje claro: `git commit -m "Add: workflow de monitoreo de APIs"`
6. **Push** a tu fork: `git push origin feature/mi-workflow`
7. **Abre un Pull Request** describiendo los cambios

### 5. 🌟 Compartir Casos de Uso
- Comparte cómo usas estos workflows en producción
- Escribe posts o tutoriales
- Da feedback sobre qué funciona y qué no

## 📋 Estándares de Código

### YAML
- Indentación: **2 espacios**
- Sin tabs
- Nombres descriptivos en español
- Comentarios explicativos

### Documentación
- Español claro y conciso
- Ejemplos prácticos
- Links a documentación oficial cuando sea relevante

## ⚠️ Qué NO hacer

- ❌ Incluir credenciales reales
- ❌ Workflows sin documentación
- ❌ Código sin probar
- ❌ Nombres genéricos o poco claros
- ❌ Duplicar workflows existentes sin mejoras

## 🔍 Revisión

Todos los PRs serán revisados considerando:
- ✅ Funcionalidad
- ✅ Documentación
- ✅ Seguridad
- ✅ Mejores prácticas de Elastic
- ✅ Utilidad para la comunidad

## 📧 Contacto

¿Dudas sobre cómo contribuir?
- Abre un [issue](https://github.com/byviz/workflows/issues)
- Contacta en [byviz.ai/contacto](https://byviz.ai/contacto)

---

**¡Gracias por hacer crecer la comunidad de Elastic en español!** 🚀

