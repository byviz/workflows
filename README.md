<div align="center">

# 🔄 Elastic Workflows
### Ejemplos Prácticos en Español (no oficial)

[![Elastic 9.3+](https://img.shields.io/badge/Elastic-9.3+-005571?style=for-the-badge&logo=elastic)](https://www.elastic.co/)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg?style=for-the-badge)](LICENSE)
[![Language](https://img.shields.io/badge/Language-Español-red?style=for-the-badge)](README.md)
[![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=for-the-badge)](https://github.com/byviz/workflows)

**Colección curada de workflows para Elastic Stack**  
Automatización end-to-end sin programación: alerting, reporting, mantenimiento, IA y más.

🌐 **[byviz.ai/workflows](https://byviz.ai/workflows)** | 💼 **[LinkedIn](https://www.linkedin.com/in/ivan-frias-molina-arquitecto-ingeniero-elasticsearch/)**

---

**Por [Iván Frías Molina](https://byviz.ai)**  
*Founder Byviz Analytics & Consulting Architect Elastic*  
Gold Contributor · Elastic Stack Specialist

</div>

---

## 📚 ¿Qué son Elastic Workflows?

**Elastic Workflows** es el motor de automatización nativo introducido en **Elastic 9.3** que permite crear procesos complejos sin programar ni usar herramientas externas.

Piensa en ellos como _"recetas automatizadas"_ definidas en **YAML** que conectan diferentes acciones:

<table>
<tr>
<td width="50%">

**🔍 Análisis de Datos**
- Búsquedas en Elasticsearch
- Agregaciones complejas
- Queries multi-índice

**🚨 Alerting Inteligente**
- Auto-respuesta a incidentes
- Notificaciones contextuales
- Escalamiento automático

</td>
<td width="50%">

**📊 Reporting Automático**
- Dashboards periódicos
- KPIs y métricas
- Envío por email/Slack

**🤖 Integración IA**
- Agentes inteligentes
- Root cause analysis
- Recomendaciones automáticas

</td>
</tr>
</table>

> 💡 **Todo dentro de tu cluster Elastic, sin infraestructura adicional**

---

## 🎯 ¿Por qué este repositorio?

Este repositorio **complementa** la [documentación oficial de Elastic](https://www.elastic.co/docs/explore-analyze/workflows) y el [repositorio oficial](https://github.com/elastic/workflows) con:

| Característica | Este Repo | Oficial Elastic |
|----------------|-----------|-----------------|
| 🌍 Idioma | **Español** | Inglés |
| 📖 Documentación | **Detallada + Contexto** | Técnica |
| 🏢 Casos de uso | **Industrias LATAM/España** | Genéricos |
| 🎓 Nivel | **Paso a paso + Producción** | Referencia |
| 🔧 Soporte | **Comunidad + Consultoría** | Oficial |

---

## 📊 Estado del Repositorio

### ✅ Disponible Ahora (Validados y Funcionales)

```
01-basicos/                         ✅ 6 workflows
├── 01-manual-trigger.yaml          → Ejecución manual
├── 02-scheduled-basic.yaml         → Programación periódica
├── 03-alert-trigger.yaml           → Disparado por alertas
├── 04-inputs-example.yaml          → Parametrización
├── 05-constants-example.yaml       → Constantes reutilizables
└── 06-templating-liquid.yaml       → Formateo avanzado
```

### 🚧 En Desarrollo (Testing y Validación)

Las siguientes categorías están siendo validadas y se liberarán progresivamente:

- 🔍 **Búsqueda y Agregación** - Queries complejas y análisis
- 🚨 **Alerting y Respuesta** - Auto-respuesta a incidentes
- 📊 **Reporting Automático** - Dashboards y KPIs
- 🧹 **Mantenimiento** - Gestión de índices y limpieza
- 🤖 **Integración IA** - Agentes inteligentes
- 🌐 **Integraciones Externas** - Slack, Teams, Jira, etc.
- 🚀 **Casos Avanzados** - Production-ready workflows

> 📅 **Actualización continua** - Sigue este repositorio para recibir notificaciones

---

## 🚀 Inicio Rápido

### Requisitos Previos

| Requisito | Versión | Notas |
|-----------|---------|-------|
| **Elastic Stack** | 9.3+ | Self-Managed o Cloud |
| **Licencia** | Enterprise | Workflows requiere Enterprise |
| **Kibana** | 9.3+ | Para gestión UI de workflows |

### 3 Pasos para tu Primer Workflow

#### **1️⃣ Accede a Workflows en Kibana**
```
Kibana → Management → Stack Management → Workflows
```

#### **2️⃣ Crea tu primer workflow**

Copia este ejemplo básico:

```yaml
name: mi-primer-workflow
description: Busca errores en logs y los muestra
enabled: true

triggers:
  - type: manual

steps:
  - name: buscar_errores
    type: elasticsearch.search
    with:
      index: "logs-*"
      query:
        match:
          level: "ERROR"
      size: 10

  - name: mostrar_resultado
    type: console
    with:
      message: |
        📊 Análisis completado
        Total errores: {{steps.buscar_errores.output.hits.total.value}}
```

#### **3️⃣ Ejecuta y verifica**
- Guarda el workflow
- Clic en **"Run"** para ejecutar manualmente
- Revisa el resultado en la consola
- ¡Tu primer workflow está funcionando! 🎉

---

## 📖 Guía de Workflows Básicos

Comienza aprendiendo los fundamentos en la carpeta [`01-basicos/`](01-basicos/):

### 🎓 Workflows Disponibles

| Workflow | Descripción | Aprenderás |
|----------|-------------|------------|
| **01-manual-trigger** | Ejecución on-demand | Triggers manuales, búsquedas básicas |
| **02-scheduled-basic** | Programación periódica | Syntax `every`, agregaciones |
| **03-alert-trigger** | Respuesta a alertas | Integración con alerting |
| **04-inputs-example** | Parametrización | Inputs dinámicos, validación |
| **05-constants-example** | Configuración reutilizable | Constantes, best practices |
| **06-templating-liquid** | Formateo avanzado | Liquid templating, loops, condicionales |

### 💡 Progresión Sugerida

```
1. Manual Trigger    → Entender la estructura básica
2. Scheduled Basic   → Aprender automatización
3. Alert Trigger     → Integrar con alerting
4. Inputs & Consts   → Hacer workflows parametrizables
5. Templating        → Dominar el formateo de salidas
```

---

## 💼 Casos de Uso por Industria

<details>
<summary><b>🏦 Banca y Fintech</b></summary>

- ✅ Monitoreo de transacciones sospechosas en tiempo real
- ✅ Alertas de fraude con contexto completo
- ✅ Auditoría automática de accesos privilegiados
- ✅ Reporting regulatorio (PSD2, GDPR, SOX)
- ✅ Detección de anomalías en pagos

</details>

<details>
<summary><b>🛒 Retail y eCommerce</b></summary>

- ✅ Análisis de comportamiento de compra
- ✅ Alertas de stock crítico con reabastecimiento
- ✅ Monitoreo de performance del checkout
- ✅ Análisis de abandono de carritos
- ✅ Detección de bots y scraping

</details>

<details>
<summary><b>🏥 Salud y Healthcare</b></summary>

- ✅ Monitoreo de sistemas críticos 24/7
- ✅ Alertas de disponibilidad de servicios vitales
- ✅ Auditoría de acceso a historiales médicos
- ✅ Reporting de incidentes y tiempos de respuesta
- ✅ Compliance con normativas sanitarias

</details>

<details>
<summary><b>🏭 Industria y Manufacturing</b></summary>

- ✅ Monitoreo de IoT y sensores industriales
- ✅ Alertas de anomalías en líneas de producción
- ✅ Mantenimiento predictivo de maquinaria
- ✅ Optimización de procesos productivos
- ✅ Control de calidad automatizado

</details>

<details>
<summary><b>🚀 Tecnología y SaaS</b></summary>

- ✅ APM y monitoreo de aplicaciones
- ✅ Alertas de latencia y errores
- ✅ Análisis de logs de microservicios
- ✅ Gestión automática de incidentes
- ✅ Dashboards para equipos DevOps

</details>

---

## 🛠️ Recursos y Aprendizaje

### 📚 Documentación

| Recurso | Descripción |
|---------|-------------|
| 📘 [Docs Oficial Elastic](https://www.elastic.co/docs/explore-analyze/workflows) | Referencia técnica completa |
| 🌐 [Landing Byviz](https://byviz.ai/workflows) | Guía y tutoriales en español |
| 💻 [Repo Oficial Elastic](https://github.com/elastic/workflows) | Ejemplos oficiales en inglés |
| 📝 [Blog Byviz](https://byviz.ai/blog) | Casos reales y tips |

### 💬 Comunidad y Soporte

- 🐛 **[Issues](https://github.com/byviz/workflows/issues)** - Reporta bugs o problemas
- 💭 **[Discussions](https://github.com/byviz/workflows/discussions)** - Comparte ideas y casos de uso
- 🤝 **[Contributing](CONTRIBUTING.md)** - Guía para contribuir
- 📧 **Contacto directo:**
  - ivan.frias@elastic.co
  - ivan.frias@byviz.com
  - [byviz.ai/contacto](https://byviz.ai/contacto)

### 🎓 Formación y Consultoría

¿Necesitas ayuda implementando workflows en tu organización?

| Servicio | Descripción |
|----------|-------------|
| 📚 **Formación Especializada** | Cursos personalizados de Elastic Workflows |
| 🏢 **Consultoría Técnica** | Diseño de arquitectura y casos de uso |
| 🔧 **Workflows Custom** | Desarrollo específico para tu stack |
| 🚀 **Migración** | Desde Watcher/Logstash a Workflows |

**[📅 Agendar consulta →](https://byviz.ai/contacto)**

---

## 🤝 Contribuir

¡Las contribuciones son bienvenidas! Este es un proyecto de la comunidad.

### Formas de Contribuir

- ✏️ **Mejora documentación** - Corrige typos, añade ejemplos
- 🐛 **Reporta bugs** - Workflows que no funcionan
- 💡 **Propón workflows** - Nuevos casos de uso
- 🌟 **Comparte experiencias** - Implementaciones reales
- 🌍 **Traducciones** - Ayuda con otros idiomas
- 📖 **Tutoriales** - Escribe guías paso a paso

Lee nuestra **[Guía de Contribución](CONTRIBUTING.md)** para empezar.

---

## 📄 Licencia

Este repositorio está bajo licencia **Apache 2.0**. Ver [LICENSE](LICENSE).

```
✅ Uso comercial permitido
✅ Modificación permitida
✅ Distribución permitida
✅ Uso privado permitido
⚠️  Incluir aviso de licencia
⚠️  Incluir aviso de copyright
```

> **Nota:** Los workflows son ejemplos educativos. Revisa y adapta según tus necesidades antes de usar en producción.

---

## ⚠️ Disclaimer Importante

- ✅ Repositorio **NO OFICIAL** - Proyecto comunitario independiente
- ⚙️ Requiere **Elastic Stack 9.3+** con **licencia Enterprise**
- 🧪 **Prueba en desarrollo** antes de producción
- 🔧 **Ajusta parámetros** según tu entorno (índices, campos, etc.)
- 🔐 **No incluye credenciales** - Usa Kibana keystore/secrets
- 📝 Workflows validados pero sin garantía - Úsalos bajo tu responsabilidad

---

## 👤 Sobre el Autor

<table>
<tr>
<td width="70%">

**Iván Frías Molina**  
*Founder Byviz Analytics & Consulting Architect Elastic*

Gold Contributor · Elastic Specialist · Solution Architect

**Especializado en:**
- 🏗️ Arquitectura y diseño de Elastic Stack
- 📊 Observabilidad, APM y Logging
- 🔒 Security Analytics (SIEM)
- 🤖 Machine Learning y detección de anomalías
- 🎓 Formación técnica y consultoría

</td>
<td width="30%">

**Contacto**

🌐 [byviz.ai](https://byviz.ai)  
💼 [LinkedIn](https://www.linkedin.com/in/ivan-frias-molina-arquitecto-ingeniero-elasticsearch/)  
📝 [Blog](https://byviz.ai/blog)  
📧 ivan.frias@elastic.co  
📧 ivan.frias@byviz.com

</td>
</tr>
</table>

---

## ⭐ ¿Te Resulta Útil?

Si este repositorio te ayuda en tus proyectos:

- ⭐ **Dale una estrella** al proyecto
- 🔄 **Comparte** en redes sociales y con tu equipo
- 🤝 **Contribuye** con tus propios workflows
- 💬 **Participa** en discussions y comparte experiencias
- 📧 **Envía feedback** para mejorar el contenido

Tu apoyo ayuda a mantener este proyecto **activo y actualizado** 💚

---

<div align="center">

**Última actualización:** Febrero 2026 | **Versión Elastic:** 9.3+  
**Workflows validados:** 6 (más en desarrollo) | **Estado:** 🟢 Activo

---

**[⬆️ Volver arriba](#-elastic-workflows)**

</div>
