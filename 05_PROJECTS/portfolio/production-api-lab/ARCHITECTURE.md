# Arquitectura

Estado: `PLANNED`.

Se propone comenzar con un monolito modular para mantener el foco en contratos, persistencia, seguridad y operación. Esta es una hipótesis de trabajo, no un ADR aceptado ni una arquitectura implementada.

## Límites a explorar

- API HTTP / DTOs
- aplicación y casos de uso
- persistencia PostgreSQL/Flyway
- Redis como dependencia opcional
- publicación de eventos y outbox
- adaptadores de observabilidad

Validar límites mediante laboratorios antes de promover decisiones a `08_DECISIONS`.
