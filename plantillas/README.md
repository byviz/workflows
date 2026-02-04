# 📋 Plantillas Reutilizables

Templates base para crear tus propios workflows rápidamente.

## 📚 Contenido

| Plantilla | Descripción | Uso |
|-----------|-------------|-----|
| `template-alerting.yaml` | Base para workflows de alerting | Copy & customize |
| `template-reporting.yaml` | Base para reportes periódicos | Copy & customize |
| `template-maintenance.yaml` | Base para tareas de mantenimiento | Copy & customize |

## 🎯 Cómo Usar

1. **Copia** la plantilla relevante
2. **Renombra** el archivo y el `name` del workflow
3. **Ajusta** índices, queries y parámetros
4. **Personaliza** los steps según tu caso de uso
5. **Testea** con trigger manual antes de automatizar

## 💡 Best Practices

- Usa `consts` para valores configurables
- Añade `inputs` para parametrización
- Documenta el propósito de cada step
- Incluye manejo de errores
- Testea con datos reales

---

**Anterior:** [08-casos-uso-avanzados](../08-casos-uso-avanzados/)

