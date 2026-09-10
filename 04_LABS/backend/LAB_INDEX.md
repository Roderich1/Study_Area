# Índice de laboratorios Backend

Estado inicial de todos los laboratorios: `PLANNED`. Esta tabla es planificación, no evidencia de ejecución.

| ID | Propósito | Sesión | Estado | Proyecto |
|---|---|---:|---|---|
| <a id="lab-backend-001-request-lifecycle"></a>LAB-BACKEND-001-request-lifecycle | Seguir DNS → TCP/TLS → HTTP → aplicación → base de datos | 01 | PLANNED | production-api-lab |
| <a id="lab-backend-002-http-conditional-requests"></a>LAB-BACKEND-002-http-conditional-requests | Probar ETag y solicitudes condicionales | 02 | PLANNED | production-api-lab |
| <a id="lab-backend-003-api-error-contract"></a>LAB-BACKEND-003-api-error-contract | Diseñar Problem Details, validación y compatibilidad | 03 | PLANNED | production-api-lab |
| <a id="lab-backend-004-postgresql-model-and-query-plan"></a>LAB-BACKEND-004-postgresql-model-and-query-plan | Diseñar el modelo relacional, cargarlo reproduciblemente y analizar consultas e índices | 04–05 | PLANNED | production-api-lab |
| <a id="lab-backend-005-lost-update"></a>LAB-BACKEND-005-lost-update | Reproducir y resolver una carrera con `stock = 1` | 06 | PLANNED | production-api-lab |
| <a id="lab-backend-006-deadlock"></a>LAB-BACKEND-006-deadlock | Observar orden de locks y recuperación segura | 06 | PLANNED | production-api-lab |
| <a id="lab-backend-007-jpa-n-plus-one"></a>LAB-BACKEND-007-jpa-n-plus-one | Detectar N+1 y evaluar carga por lotes | 07 | PLANNED | production-api-lab |
| <a id="lab-backend-008-bola-authorization"></a>LAB-BACKEND-008-bola-authorization | Verificar autorización por objeto y propiedad | 08–09 | PLANNED | production-api-lab |
| <a id="lab-backend-009-idempotency-key"></a>LAB-BACKEND-009-idempotency-key | Garantizar un único efecto lógico de un pago repetido | 10 | PLANNED | production-api-lab |
| <a id="lab-backend-010-redis-cache"></a>LAB-BACKEND-010-redis-cache | Comparar latencia, TTL, invalidación y datos stale | 11 | PLANNED | production-api-lab |
| <a id="lab-backend-011-testcontainers-postgresql"></a>LAB-BACKEND-011-testcontainers-postgresql | Probar contra PostgreSQL real y aislar fixtures | 13 | PLANNED | production-api-lab |
| <a id="lab-backend-012-service-timeout"></a>LAB-BACKEND-012-service-timeout | Simular dependencia lenta y retries acotados | 10 | PLANNED | production-api-lab |
| <a id="lab-backend-013-transactional-outbox"></a>LAB-BACKEND-013-transactional-outbox | Coordinar escritura de datos y evento | 12 | PLANNED | production-api-lab |
| <a id="lab-backend-014-containerized-stack"></a>LAB-BACKEND-014-containerized-stack | Empaquetar API, PostgreSQL, Redis y healthchecks | 14 | PLANNED | production-api-lab |
| <a id="lab-backend-015-observability-diagnosis"></a>LAB-BACKEND-015-observability-diagnosis | Diagnosticar endpoint lento con logs, métricas y trazas | 15 | PLANNED | production-api-lab |

## LAB-BACKEND-004 — Modelo PostgreSQL y plan de consultas

Este laboratorio transversal permanece en estado `PLANNED` y conecta las sesiones 04 y 05 sobre el mismo esquema:

### Sesión 04 — Modelo y migraciones

Diseñar el modelo relacional inicial, definir PK/FK, `UNIQUE`, `CHECK` y `NOT NULL`, revisar la normalización, crear migraciones Flyway y cargar el esquema de forma reproducible.

### Sesión 05 — Queries, coste e índices

Crear un dataset, ejecutar queries, leer `EXPLAIN ANALYZE`, identificar el coste, diseñar un índice y comparar el comportamiento antes y después.

## Convención de materialización

Cuando un laboratorio se ejecute, crear su carpeta bajo `04_LABS/backend/` con `README.md`, `commands.md`, `results.md`, `troubleshooting.md`, `rollback.md` y `evidence/`. Enlazarlo desde esta tabla y actualizar el estado solo con resultados verificables.
