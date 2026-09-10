# Ejercicios — Sesión 13

Intenta resolverlos antes de consultar soluciones. Registra razonamiento, supuestos y evidencia; las respuestas no se proporcionan automáticamente.

## Comprensión

1. Explica con un diagrama cómo se relacionan los conceptos de unit, integration, repository, API, security y contract tests, failure testing, Testcontainers, PostgreSQL real, isolation, fixtures y determinismo.
2. ¿Qué garantía ofrece la solución principal y qué caso límite deja sin resolver?
3. Compara dos alternativas del tema y justifica cuándo elegirías cada una.

## Diseño

4. Diseña cómo aplicarías el tema a production-api-lab sin mezclar responsabilidades entre API, persistencia y operación.
5. Define una métrica, restricción o contrato que permita comprobar que tu diseño se comporta como esperas.

## Diagnóstico

6. Un comportamiento del laboratorio no coincide con la hipótesis. Propón observaciones, comandos o pruebas para aislar la causa antes de cambiar código.

## Implementación práctica

7. Implementa el escenario mínimo del laboratorio **LAB-BACKEND-011-testcontainers-postgresql** y registra resultado esperado frente a resultado real.
8. Rompe o estresa el escenario de forma controlada, aplica una solución y vuelve a medir.

## PostgreSQL real

- Ejecuta el mismo caso contra un contenedor PostgreSQL real, no contra una base embebida que oculte diferencias.
- Aísla fixtures entre pruebas y añade un caso de concurrencia, autorización o constraint que pueda fallar de forma determinista.
- Registra la versión de la imagen y el comando de ejecución como parte de la evidencia.

## Decisión técnica

9. Escribe una recomendación breve con contexto, opciones, trade-offs, decisión provisional y cómo la verificarías. No la conviertas en ADR hasta que exista una decisión real aceptada.
