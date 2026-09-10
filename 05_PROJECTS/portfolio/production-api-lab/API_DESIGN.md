# Diseño de API

Estado: `PLANNED`.

El contrato evolucionará desde las sesiones 01–03 y se describirá con OpenAPI. Se decidirán URI, DTOs, validación, Problem Details, paginación, filtering, sorting, versioning, ETags y compatibilidad hacia atrás antes de declarar endpoints verificados.

## Flujos candidatos

- catálogo de productos;
- inventario;
- creación y consulta de pedidos;
- pago idempotente;
- health y observabilidad operativa.

Separar contrato público de entidades JPA. Los ejemplos definitivos se agregarán cuando exista una implementación verificable.
