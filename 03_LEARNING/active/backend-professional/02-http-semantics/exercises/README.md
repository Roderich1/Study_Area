# Ejercicios — Sesión 02

Intenta resolverlos antes de consultar soluciones. Registra razonamiento, supuestos y evidencia; las respuestas no se proporcionan automáticamente.

## Comprensión

1. Explica con un diagrama cómo se relacionan los conceptos de GET, POST, PUT, PATCH, DELETE, HEAD, OPTIONS, safe, idempotency, status codes, headers, content negotiation, caching, ETag, If-Match, If-None-Match y conditional requests.
2. ¿Qué garantía ofrece la solución principal y qué caso límite deja sin resolver?
3. Compara dos alternativas del tema y justifica cuándo elegirías cada una.

## Diseño

4. Diseña cómo aplicarías el tema a production-api-lab sin mezclar responsabilidades entre API, persistencia y operación.
5. Define una métrica, restricción o contrato que permita comprobar que tu diseño se comporta como esperas.

## Diagnóstico

6. Un comportamiento del laboratorio no coincide con la hipótesis. Propón observaciones, comandos o pruebas para aislar la causa antes de cambiar código.

## Implementación práctica

7. Implementa el escenario mínimo del laboratorio **LAB-BACKEND-002-http-conditional-requests** y registra resultado esperado frente a resultado real.
8. Rompe o estresa el escenario de forma controlada, aplica una solución y vuelve a medir.

## Casos HTTP obligatorios

- Construye una tabla de decisión para `PUT` frente a `PATCH`, incluyendo reemplazo, actualización parcial, reintentos e idempotencia.
- Explica con ejemplos cuándo corresponde `401` frente a `403`.
- Diseña respuestas para `409` frente a `422` y justifica qué conflicto o error de validación representa cada una.
- Clasifica varios métodos como *safe*, *idempotent* o ambos y explica por qué la seguridad no implica idempotencia.

## Decisión técnica

9. Escribe una recomendación breve con contexto, opciones, trade-offs, decisión provisional y cómo la verificarías. No la conviertas en ADR hasta que exista una decisión real aceptada.
