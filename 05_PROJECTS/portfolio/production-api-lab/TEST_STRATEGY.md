# Estrategia de pruebas

Estado: `PLANNED`.

Combinar pruebas unitarias, de integración, repositorio, API, seguridad y contrato según el riesgo. Testcontainers deberá proporcionar PostgreSQL real para evitar que una base distinta esconda incompatibilidades.

## Criterios de verificación

- aislamiento y fixtures deterministas;
- pruebas de concurrencia e idempotencia;
- fallos de dependencias y timeouts;
- regresiones de autorización;
- evidencia reproducible sin secretos.
