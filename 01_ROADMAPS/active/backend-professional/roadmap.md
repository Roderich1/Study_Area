# Backend Professional Roadmap

## Cómo usarlo

Avanza en orden, manteniendo la separación entre aprendizaje activo, laboratorios y proyecto. Cada sesión enlaza su módulo, el laboratorio planificado y el proyecto transversal. Los estados deben actualizarse solo después de evidencia real.

## Dependencias globales

Las sesiones 01—03 establecen red y contratos; 04—07 establecen persistencia y concurrencia; 08—10 seguridad y fiabilidad; 11—12 rendimiento y asincronía; 13—15 validación, despliegue y diagnóstico. La sesión 06 es prerrequisito conceptual para 07 y 10; 03 y 04 son prerrequisitos para 05; 08 precede 09; 13 se apoya en 04 y 08; 14 y 15 integran todo lo anterior.

## Sesiones
### Sesión 01 — Backend Request Lifecycle

- **Objetivo:** Explicar de extremo a extremo qué ocurre desde que un cliente inicia una petición hasta que recibe una respuesta.
- **Conceptos:** cliente-servidor, DNS, TCP, TLS, HTTP, puertos, reverse proxy, application server, threads/processes, ciclo de conexión, ciclo de request, base de datos y statelessness.
- **Ejercicios:** recuperación activa, análisis de un caso de producción, implementación en production-api-lab, diagnóstico de una falla intencional y defensa de un trade-off.
- **Laboratorio:** [LAB-BACKEND-001-request-lifecycle](../../../04_LABS/backend/LAB_INDEX.md#lab-backend-001-request-lifecycle) — trazar una petición desde DNS hasta la respuesta y correlacionarla con una consulta a PostgreSQL.
- **Entregables:** notas provisionales, ejercicios resueltos, evidencia del laboratorio cuando se ejecute, actualización del proyecto y [checkpoint](../../../03_LEARNING/active/backend-professional/01-backend-request-lifecycle/checkpoint.md).
- **Recursos:** comenzar por la documentación oficial enlazada en [Backend Resources](../../../09_RESOURCES/backend-resources.md); elegir solo lo necesario para la pregunta de la sesión.
- **Dependencias:** respetar las dependencias globales anteriores y consultar el README de la sesión.
### Sesión 02 — HTTP Semantics

- **Objetivo:** Elegir métodos, códigos y headers HTTP que expresen correctamente la semántica de una API.
- **Conceptos:** GET, POST, PUT, PATCH, DELETE, HEAD, OPTIONS, safe, idempotency, status codes, headers, content negotiation, caching, ETag, If-Match, If-None-Match y conditional requests.
- **Ejercicios:** recuperación activa, análisis de un caso de producción, implementación en production-api-lab, diagnóstico de una falla intencional y defensa de un trade-off.
- **Laboratorio:** [LAB-BACKEND-002-http-conditional-requests](../../../04_LABS/backend/LAB_INDEX.md#lab-backend-002-http-conditional-requests) — diseñar y probar solicitudes condicionales, comparando PUT/PATCH, 401/403 y 409/422.
- **Entregables:** notas provisionales, ejercicios resueltos, evidencia del laboratorio cuando se ejecute, actualización del proyecto y [checkpoint](../../../03_LEARNING/active/backend-professional/02-http-semantics/checkpoint.md).
- **Recursos:** comenzar por la documentación oficial enlazada en [Backend Resources](../../../09_RESOURCES/backend-resources.md); elegir solo lo necesario para la pregunta de la sesión.
- **Dependencias:** respetar las dependencias globales anteriores y consultar el README de la sesión.
### Sesión 03 — Professional API Design

- **Objetivo:** Diseñar contratos de API evolutivos, claros y compatibles hacia atrás.
- **Conceptos:** resource modeling, URI design, DTOs, contratos, validación, Problem Details, paginación, cursor pagination, filtering, sorting, versioning, OpenAPI y backward compatibility.
- **Ejercicios:** recuperación activa, análisis de un caso de producción, implementación en production-api-lab, diagnóstico de una falla intencional y defensa de un trade-off.
- **Laboratorio:** [LAB-BACKEND-003-api-error-contract](../../../04_LABS/backend/LAB_INDEX.md#lab-backend-003-api-error-contract) — convertir requisitos del proyecto transversal en un contrato OpenAPI con errores consistentes.
- **Entregables:** notas provisionales, ejercicios resueltos, evidencia del laboratorio cuando se ejecute, actualización del proyecto y [checkpoint](../../../03_LEARNING/active/backend-professional/03-api-design/checkpoint.md).
- **Recursos:** comenzar por la documentación oficial enlazada en [Backend Resources](../../../09_RESOURCES/backend-resources.md); elegir solo lo necesario para la pregunta de la sesión.
- **Dependencias:** respetar las dependencias globales anteriores y consultar el README de la sesión.
### Sesión 04 — Relational Data Modeling

- **Objetivo:** Modelar datos relacionales con integridad explícita y migraciones reproducibles.
- **Conceptos:** entities, relationships, PK, FK, UNIQUE, CHECK, NOT NULL, normalization, denormalization, integridad, schema evolution y Flyway.
- **Ejercicios:** recuperación activa, análisis de un caso de producción, implementación en production-api-lab, diagnóstico de una falla intencional y defensa de un trade-off.
- **Laboratorio:** [LAB-BACKEND-004-postgresql-query-plan](../../../04_LABS/backend/LAB_INDEX.md#lab-backend-004-postgresql-query-plan) — proponer el modelo inicial de production-api-lab y una secuencia segura de migraciones.
- **Entregables:** notas provisionales, ejercicios resueltos, evidencia del laboratorio cuando se ejecute, actualización del proyecto y [checkpoint](../../../03_LEARNING/active/backend-professional/04-data-modeling/checkpoint.md).
- **Recursos:** comenzar por la documentación oficial enlazada en [Backend Resources](../../../09_RESOURCES/backend-resources.md); elegir solo lo necesario para la pregunta de la sesión.
- **Dependencias:** respetar las dependencias globales anteriores y consultar el README de la sesión.
### Sesión 05 — SQL, Query Planning & Indexes

- **Objetivo:** Leer planes de ejecución y justificar índices según selectividad, cardinalidad y coste.
- **Conceptos:** JOIN, GROUP BY, subqueries, CTE, EXPLAIN, EXPLAIN ANALYZE, B-tree, índices compuestos, parciales y covering, selectivity, cardinality y trade-offs.
- **Ejercicios:** recuperación activa, análisis de un caso de producción, implementación en production-api-lab, diagnóstico de una falla intencional y defensa de un trade-off.
- **Laboratorio:** [LAB-BACKEND-004-postgresql-query-plan](../../../04_LABS/backend/LAB_INDEX.md#lab-backend-004-postgresql-query-plan) — comparar una consulta lenta antes y después de un índice usando PostgreSQL real.
- **Entregables:** notas provisionales, ejercicios resueltos, evidencia del laboratorio cuando se ejecute, actualización del proyecto y [checkpoint](../../../03_LEARNING/active/backend-professional/05-sql-indexes/checkpoint.md).
- **Recursos:** comenzar por la documentación oficial enlazada en [Backend Resources](../../../09_RESOURCES/backend-resources.md); elegir solo lo necesario para la pregunta de la sesión.
- **Dependencias:** respetar las dependencias globales anteriores y consultar el README de la sesión.
### Sesión 06 — Transactions & Concurrency

- **Objetivo:** Explicar y controlar anomalías de concurrencia en operaciones transaccionales.
- **Conceptos:** ACID, transactions, MVCC, isolation levels, Read Committed, Repeatable Read, Serializable, dirty/non-repeatable/phantom reads, lost updates, locks, deadlocks, race conditions y locking optimista/pesimista.
- **Ejercicios:** recuperación activa, análisis de un caso de producción, implementación en production-api-lab, diagnóstico de una falla intencional y defensa de un trade-off.
- **Laboratorio:** [LAB-BACKEND-005-lost-update](../../../04_LABS/backend/LAB_INDEX.md#lab-backend-005-lost-update) — reproducir el caso stock=1 con dos compras concurrentes y justificar la solución.
- **Entregables:** notas provisionales, ejercicios resueltos, evidencia del laboratorio cuando se ejecute, actualización del proyecto y [checkpoint](../../../03_LEARNING/active/backend-professional/06-transactions-concurrency/checkpoint.md).
- **Recursos:** comenzar por la documentación oficial enlazada en [Backend Resources](../../../09_RESOURCES/backend-resources.md); elegir solo lo necesario para la pregunta de la sesión.
- **Dependencias:** respetar las dependencias globales anteriores y consultar el README de la sesión.
### Sesión 07 — ORM & Persistence

- **Objetivo:** Entender qué hace JPA/Hibernate y evitar costes ocultos de persistencia.
- **Conceptos:** ORM, JPA/Hibernate, entity lifecycle, persistence context, transactions, lazy/eager loading, N+1, batching, optimistic locking y connection pools.
- **Ejercicios:** recuperación activa, análisis de un caso de producción, implementación en production-api-lab, diagnóstico de una falla intencional y defensa de un trade-off.
- **Laboratorio:** [LAB-BACKEND-007-jpa-n-plus-one](../../../04_LABS/backend/LAB_INDEX.md#lab-backend-007-jpa-n-plus-one) — observar SQL generado por Hibernate, detectar N+1 y comparar alternativas de carga.
- **Entregables:** notas provisionales, ejercicios resueltos, evidencia del laboratorio cuando se ejecute, actualización del proyecto y [checkpoint](../../../03_LEARNING/active/backend-professional/07-orm-persistence/checkpoint.md).
- **Recursos:** comenzar por la documentación oficial enlazada en [Backend Resources](../../../09_RESOURCES/backend-resources.md); elegir solo lo necesario para la pregunta de la sesión.
- **Dependencias:** respetar las dependencias globales anteriores y consultar el README de la sesión.
### Sesión 08 — Authentication & Authorization

- **Objetivo:** Separar identidad, autenticación y autorización al proteger recursos de una API.
- **Conceptos:** authentication, authorization, sessions, cookies, access/refresh tokens, JWT, OAuth, OpenID Connect, issuer, audience, scopes, roles, permissions, Resource Server y Authorization Server.
- **Ejercicios:** recuperación activa, análisis de un caso de producción, implementación en production-api-lab, diagnóstico de una falla intencional y defensa de un trade-off.
- **Laboratorio:** [LAB-BACKEND-008-bola-authorization](../../../04_LABS/backend/LAB_INDEX.md#lab-backend-008-bola-authorization) — proteger endpoints del proyecto con un modelo de identidad y permisos explícito.
- **Entregables:** notas provisionales, ejercicios resueltos, evidencia del laboratorio cuando se ejecute, actualización del proyecto y [checkpoint](../../../03_LEARNING/active/backend-professional/08-authentication-authorization/checkpoint.md).
- **Recursos:** comenzar por la documentación oficial enlazada en [Backend Resources](../../../09_RESOURCES/backend-resources.md); elegir solo lo necesario para la pregunta de la sesión.
- **Dependencias:** respetar las dependencias globales anteriores y consultar el README de la sesión.
### Sesión 09 — API Security

- **Objetivo:** Identificar y mitigar riesgos frecuentes de seguridad en APIs.
- **Conceptos:** OWASP API Security, BOLA/IDOR, broken authentication, property authorization, mass assignment, SQL injection, SSRF, CORS, CSRF, rate limiting, secrets, password hashing, headers, least privilege y threat modeling.
- **Ejercicios:** recuperación activa, análisis de un caso de producción, implementación en production-api-lab, diagnóstico de una falla intencional y defensa de un trade-off.
- **Laboratorio:** [LAB-BACKEND-008-bola-authorization](../../../04_LABS/backend/LAB_INDEX.md#lab-backend-008-bola-authorization) — ejecutar un ataque controlado de autorización sobre recursos propios y documentar la mitigación.
- **Entregables:** notas provisionales, ejercicios resueltos, evidencia del laboratorio cuando se ejecute, actualización del proyecto y [checkpoint](../../../03_LEARNING/active/backend-professional/09-api-security/checkpoint.md).
- **Recursos:** comenzar por la documentación oficial enlazada en [Backend Resources](../../../09_RESOURCES/backend-resources.md); elegir solo lo necesario para la pregunta de la sesión.
- **Dependencias:** respetar las dependencias globales anteriores y consultar el README de la sesión.
### Sesión 10 — Reliability, Retries & Idempotency

- **Objetivo:** Diseñar operaciones resistentes a timeouts, reintentos y duplicación de solicitudes.
- **Conceptos:** failure modes, timeouts, retries, exponential backoff, jitter, idempotency keys, duplicate requests, circuit breakers y dependencias externas.
- **Ejercicios:** recuperación activa, análisis de un caso de producción, implementación en production-api-lab, diagnóstico de una falla intencional y defensa de un trade-off.
- **Laboratorio:** [LAB-BACKEND-009-idempotency-key](../../../04_LABS/backend/LAB_INDEX.md#lab-backend-009-idempotency-key) — hacer que POST /payments produzca un único efecto lógico para una misma Idempotency-Key.
- **Entregables:** notas provisionales, ejercicios resueltos, evidencia del laboratorio cuando se ejecute, actualización del proyecto y [checkpoint](../../../03_LEARNING/active/backend-professional/10-reliability-idempotency/checkpoint.md).
- **Recursos:** comenzar por la documentación oficial enlazada en [Backend Resources](../../../09_RESOURCES/backend-resources.md); elegir solo lo necesario para la pregunta de la sesión.
- **Dependencias:** respetar las dependencias globales anteriores y consultar el README de la sesión.
### Sesión 11 — Redis & Caching

- **Objetivo:** Aplicar cache-aside y medir cuándo una caché mejora el sistema sin ocultar problemas de consistencia.
- **Conceptos:** caching, cache-aside, TTL, invalidation, cache stampede, stale data, distributed cache, Redis, sessions y rate limiting.
- **Ejercicios:** recuperación activa, análisis de un caso de producción, implementación en production-api-lab, diagnóstico de una falla intencional y defensa de un trade-off.
- **Laboratorio:** [LAB-BACKEND-010-redis-cache](../../../04_LABS/backend/LAB_INDEX.md#lab-backend-010-redis-cache) — medir latencia antes/después, invalidar datos y explicar los riesgos de stale data.
- **Entregables:** notas provisionales, ejercicios resueltos, evidencia del laboratorio cuando se ejecute, actualización del proyecto y [checkpoint](../../../03_LEARNING/active/backend-professional/11-caching-redis/checkpoint.md).
- **Recursos:** comenzar por la documentación oficial enlazada en [Backend Resources](../../../09_RESOURCES/backend-resources.md); elegir solo lo necesario para la pregunta de la sesión.
- **Dependencias:** respetar las dependencias globales anteriores y consultar el README de la sesión.
### Sesión 12 — Asynchronous Processing & Events

- **Objetivo:** Distinguir procesamiento síncrono y asíncrono y diseñar entrega de eventos con consistencia eventual.
- **Conceptos:** synchronous/asynchronous processing, queues, events, workers, at-most-once, at-least-once, duplicate delivery, eventual consistency, transactional outbox y dead-letter queues.
- **Ejercicios:** recuperación activa, análisis de un caso de producción, implementación en production-api-lab, diagnóstico de una falla intencional y defensa de un trade-off.
- **Laboratorio:** [LAB-BACKEND-013-transactional-outbox](../../../04_LABS/backend/LAB_INDEX.md#lab-backend-013-transactional-outbox) — modelar una publicación de evento confiable sin introducir Kafka profundamente.
- **Entregables:** notas provisionales, ejercicios resueltos, evidencia del laboratorio cuando se ejecute, actualización del proyecto y [checkpoint](../../../03_LEARNING/active/backend-professional/12-async-processing/checkpoint.md).
- **Recursos:** comenzar por la documentación oficial enlazada en [Backend Resources](../../../09_RESOURCES/backend-resources.md); elegir solo lo necesario para la pregunta de la sesión.
- **Dependencias:** respetar las dependencias globales anteriores y consultar el README de la sesión.
### Sesión 13 — Professional Testing

- **Objetivo:** Construir pruebas deterministas que detecten diferencias reales de PostgreSQL y seguridad.
- **Conceptos:** unit, integration, repository, API, security y contract tests, failure testing, Testcontainers, PostgreSQL real, isolation, fixtures y determinismo.
- **Ejercicios:** recuperación activa, análisis de un caso de producción, implementación en production-api-lab, diagnóstico de una falla intencional y defensa de un trade-off.
- **Laboratorio:** [LAB-BACKEND-011-testcontainers-postgresql](../../../04_LABS/backend/LAB_INDEX.md#lab-backend-011-testcontainers-postgresql) — probar el flujo principal con Testcontainers y aislar datos sin depender de una base falsa.
- **Entregables:** notas provisionales, ejercicios resueltos, evidencia del laboratorio cuando se ejecute, actualización del proyecto y [checkpoint](../../../03_LEARNING/active/backend-professional/13-testing/checkpoint.md).
- **Recursos:** comenzar por la documentación oficial enlazada en [Backend Resources](../../../09_RESOURCES/backend-resources.md); elegir solo lo necesario para la pregunta de la sesión.
- **Dependencias:** respetar las dependencias globales anteriores y consultar el README de la sesión.
### Sesión 14 — Docker & Deployment

- **Objetivo:** Empaquetar y desplegar el servicio con configuración explícita, healthchecks y rollback.
- **Conceptos:** Dockerfile, multi-stage builds, images, containers, Compose, environment variables, configuration, secrets, healthchecks, readiness, liveness, reverse proxy, TLS, deployment y rollback.
- **Ejercicios:** recuperación activa, análisis de un caso de producción, implementación en production-api-lab, diagnóstico de una falla intencional y defensa de un trade-off.
- **Laboratorio:** [LAB-BACKEND-014-containerized-stack](../../../04_LABS/backend/LAB_INDEX.md#lab-backend-014-containerized-stack) — levantar una topología reproducible de API, PostgreSQL, Redis y reverse proxy sin secretos reales.
- **Entregables:** notas provisionales, ejercicios resueltos, evidencia del laboratorio cuando se ejecute, actualización del proyecto y [checkpoint](../../../03_LEARNING/active/backend-professional/14-deployment/checkpoint.md).
- **Recursos:** comenzar por la documentación oficial enlazada en [Backend Resources](../../../09_RESOURCES/backend-resources.md); elegir solo lo necesario para la pregunta de la sesión.
- **Dependencias:** respetar las dependencias globales anteriores y consultar el README de la sesión.
### Sesión 15 — Observability & Production Diagnosis

- **Objetivo:** Investigar una degradación desde señales observables hasta la causa y medir la mejora.
- **Conceptos:** structured logs, correlation/request IDs, metrics, RED, traces, spans, distributed tracing, OpenTelemetry, Micrometer, Actuator, health endpoints y performance investigation.
- **Ejercicios:** recuperación activa, análisis de un caso de producción, implementación en production-api-lab, diagnóstico de una falla intencional y defensa de un trade-off.
- **Laboratorio:** [LAB-BACKEND-015-observability-diagnosis](../../../04_LABS/backend/LAB_INDEX.md#lab-backend-015-observability-diagnosis) — seguir endpoint lento -> trace -> query -> EXPLAIN ANALYZE -> optimización -> nueva medición.
- **Entregables:** notas provisionales, ejercicios resueltos, evidencia del laboratorio cuando se ejecute, actualización del proyecto y [checkpoint](../../../03_LEARNING/active/backend-professional/15-observability/checkpoint.md).
- **Recursos:** comenzar por la documentación oficial enlazada en [Backend Resources](../../../09_RESOURCES/backend-resources.md); elegir solo lo necesario para la pregunta de la sesión.
- **Dependencias:** respetar las dependencias globales anteriores y consultar el README de la sesión.
## Criterios de finalización

- Cada sesión alcanza el criterio de su checkpoint con promedio mínimo 4/5.
- Los laboratorios se ejecutan y documentan con resultados reales, sin rellenar resultados por anticipado.
- `production-api-lab` distingue `PLANNED`, `IMPLEMENTED` y `VERIFIED` y cuenta con pruebas y evidencias.
- Se promueven a `02_KNOWLEDGE` únicamente conceptos realmente consolidados.
- No se crean incidentes, ADRs ni runbooks ficticios.
