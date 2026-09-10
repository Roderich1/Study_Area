# Requisitos

Estado global: `PLANNED`.

## Funcionales

- Gestionar usuarios, productos e inventario.
- Crear pedidos con sus líneas.
- Registrar pagos de forma idempotente.
- Exponer contratos HTTP versionables y errores Problem Details.
- Emitir eventos de dominio cuando el diseño y la consistencia lo requieran.

## No funcionales para practicar

- Integridad relacional y migraciones.
- Autorización por objeto y propiedad.
- Límites de timeout, retries e idempotencia.
- Pruebas deterministas contra PostgreSQL.
- Healthchecks, métricas, logs estructurados y trazas.

Estos requisitos no implican que exista implementación. Cada uno se verificará en el hito correspondiente.
