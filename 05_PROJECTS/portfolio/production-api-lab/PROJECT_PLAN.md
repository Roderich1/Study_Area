# Plan del proyecto

## Objetivo

Usar un único sistema incremental para convertir cada sesión del roadmap en una capacidad observable. Cada cambio debe indicar si está `PLANNED`, `IMPLEMENTED` o `VERIFIED`.

## Secuencia

1. Request lifecycle y contrato inicial.
2. Modelo relacional y migraciones.
3. Consultas, índices y transacciones.
4. Autenticación, autorización y seguridad.
5. Idempotencia, caché y eventos.
6. Pruebas con PostgreSQL real.
7. Contenedores, despliegue y observabilidad.

## Regla de evidencia

Un estado `IMPLEMENTED` requiere código presente; `VERIFIED` requiere una prueba, medición o experimento reproducible enlazado. Hasta entonces el documento es planificación.
