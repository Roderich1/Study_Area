# Backend Resources

Índice curado para Backend Professional. Prioriza documentación oficial y no descarga material masivo al Knowledge Lab. Estado inicial de cada recurso: `Referencia` o `Pendiente`.

Formato: **Nombre** — URL · Autor/organización · Nivel · Tema · Por qué vale la pena · Estado.

## HTTP

- **MDN HTTP overview** — https://developer.mozilla.org/en-US/docs/Web/HTTP/Overview · MDN · Intermedio · HTTP · explicación práctica del flujo web · Referencia.
- **RFC 9110 — HTTP Semantics** — https://www.rfc-editor.org/rfc/rfc9110 · IETF · Avanzado · semántica HTTP, métodos, status y caching · fuente normativa · Referencia.
- **MDN Conditional requests** — https://developer.mozilla.org/en-US/docs/Web/HTTP/Conditional_requests · MDN · Intermedio · ETag y validadores · guía de experimentos · Pendiente.

## REST / API Design

- **RFC 9457 — Problem Details** — https://www.rfc-editor.org/rfc/rfc9457 · IETF · Intermedio · contratos de error · formato estándar interoperable · Referencia.
- **OpenAPI Specification** — https://spec.openapis.org/oas/latest.html · OpenAPI Initiative · Intermedio · contratos y tooling · fuente del formato · Referencia.

## PostgreSQL

- **PostgreSQL documentation** — https://www.postgresql.org/docs/current/ · PostgreSQL Global Development Group · Intermedio/Avanzado · SQL, constraints y operación · fuente primaria · Referencia.
- **Constraints** — https://www.postgresql.org/docs/current/ddl-constraints.html · PostgreSQL Global Development Group · Intermedio · integridad · explica garantías en la base · Pendiente.
- **EXPLAIN** — https://www.postgresql.org/docs/current/sql-explain.html · PostgreSQL Global Development Group · Intermedio · planes e índices · imprescindible para diagnóstico · Pendiente.

## Transactions & Concurrency

- **Transaction isolation** — https://www.postgresql.org/docs/current/transaction-iso.html · PostgreSQL Global Development Group · Avanzado · MVCC y niveles de aislamiento · conecta teoría con PostgreSQL · Pendiente.
- **Designing Data-Intensive Applications** — https://dataintensive.net/ · Martin Kleppmann · Avanzado · sistemas distribuidos y datos · profundización conceptual · Pendiente.

## Spring Boot

- **Spring Boot Reference** — https://docs.spring.io/spring-boot/reference/ · VMware Tanzu/Spring · Intermedio · configuración, testing y Actuator · fuente oficial · Referencia.
- **Spring Data JPA** — https://docs.spring.io/spring-data/jpa/reference/ · Spring · Intermedio · repositorios y persistencia · relación entre abstracción y JPA · Pendiente.
- **Hibernate ORM documentation** — https://hibernate.org/orm/documentation/ · Hibernate · Avanzado · persistence context y SQL · entender costes del ORM · Pendiente.

## Spring Security

- **Spring Security Reference** — https://docs.spring.io/spring-security/reference/ · Spring · Intermedio/Avanzado · autenticación y autorización · implementación de referencia · Referencia.

## OAuth / OIDC

- **OpenID Connect how it works** — https://openid.net/developers/how-connect-works/ · OpenID Foundation · Intermedio · identidad y tokens · modelo de issuer/audience/scopes · Pendiente.
- **OAuth 2.0 RFC 6749** — https://www.rfc-editor.org/rfc/rfc6749 · IETF · Avanzado · autorización delegada · especificación primaria · Referencia.

## API Security

- **OWASP API Security Top 10** — https://owasp.github.io/www-project-api-security/ · OWASP · Intermedio · amenazas de API · catálogo para threat modeling · Referencia.
- **OWASP Cheat Sheet Series** — https://cheatsheetseries.owasp.org/ · OWASP · Intermedio · mitigaciones · referencias accionables · Pendiente.

## Redis

- **Redis Documentation** — https://redis.io/docs/latest/ · Redis · Intermedio · caching, TTL y estructuras · fuente primaria · Referencia.
- **Spring Data Redis** — https://docs.spring.io/spring-data/redis/reference/ · Spring · Intermedio · integración Java · guía oficial · Pendiente.

## Testing

- **Testcontainers for Java** — https://java.testcontainers.org/ · Testcontainers · Intermedio · dependencias reales en tests · evita falsos positivos de bases simuladas · Referencia.
- **Spring Boot testing** — https://docs.spring.io/spring-boot/reference/testing/index.html · Spring · Intermedio · estrategia de pruebas · integración con el stack · Pendiente.

## Docker

- **Docker Documentation** — https://docs.docker.com/ · Docker · Intermedio · imágenes, Compose y operación · fuente primaria · Referencia.
- **Spring Boot container images** — https://docs.spring.io/spring-boot/reference/packaging/container-images/index.html · Spring · Intermedio · empaquetado · conecta Java con contenedores · Pendiente.

## Observability

- **OpenTelemetry Documentation** — https://opentelemetry.io/docs/ · CNCF/OpenTelemetry · Intermedio/Avanzado · traces, metrics y context · estándar abierto · Referencia.
- **Spring Boot Actuator** — https://docs.spring.io/spring-boot/reference/actuator/index.html · Spring · Intermedio · health y métricas · instrumentación del servicio · Pendiente.
- **Micrometer** — https://micrometer.io/docs · Micrometer · Intermedio · métricas JVM y aplicación · fachada de métricas · Pendiente.

## Distributed Systems

- **Transactional Outbox pattern** — https://microservices.io/patterns/data/transactional-outbox.html · Chris Richardson · Avanzado · eventos y consistencia · patrón del laboratorio 013 · Pendiente.
- **Spring transaction-bound events** — https://docs.spring.io/spring-framework/reference/data-access/transaction/event.html · Spring · Avanzado · eventos ligados a transacciones · implementación de referencia · Pendiente.

## Books

- **Designing Data-Intensive Applications** — https://dataintensive.net/ · Martin Kleppmann · Avanzado · datos, consistencia y sistemas distribuidos · profundización recomendada · Pendiente.
