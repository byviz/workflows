# 🔍 Búsqueda y Agregación

Workflows para queries complejas, agregaciones y análisis de datos en Elasticsearch.

## 📚 Contenido

| Workflow | Descripción | Complejidad |
|----------|-------------|-------------|
| `01-search-basic.yaml` | Búsquedas simples con filtros | ⭐ |
| `02-search-multi-index.yaml` | Búsqueda en múltiples índices | ⭐⭐ |
| `03-aggregations-basic.yaml` | Agregaciones términos y métricas | ⭐⭐ |
| `04-aggregations-advanced.yaml` | Agregaciones anidadas y buckets | ⭐⭐⭐ |
| `05-time-series-analysis.yaml` | Análisis de series temporales | ⭐⭐⭐ |
| `06-full-text-search.yaml` | Búsqueda full-text avanzada | ⭐⭐ |

## 🎯 Qué aprenderás

### Búsquedas
- Match queries
- Bool queries (must, should, filter)
- Range queries para fechas
- Multi-index patterns
- Sorting y paginación

### Agregaciones
- Terms aggregations
- Date histogram
- Metrics (sum, avg, max, min)
- Buckets anidados
- Pipeline aggregations

### Análisis
- Tendencias temporales
- Top N resultados
- Estadísticas descriptivas
- Correlaciones

## 💡 Tips

- Usa `size: 0` cuando solo quieras agregaciones
- Los filtros en `bool` queries son más rápidos
- Date histograms son perfectos para time series
- Combina búsquedas con agregaciones para análisis potentes

## 📖 Referencias

- [Elasticsearch Query DSL](https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl.html)
- [Aggregations](https://www.elastic.co/guide/en/elasticsearch/reference/current/search-aggregations.html)

---

**Anterior:** [01-basicos](../01-basicos/) | **Siguiente:** [03-alerting-respuesta](../03-alerting-respuesta/)

