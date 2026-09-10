# Ejercicios — Sesión 10

Intenta resolverlos antes de consultar soluciones. Registra razonamiento, supuestos y evidencia; las respuestas no se proporcionan automáticamente.

## Comprensión

1. Explica con un diagrama cómo se relacionan los conceptos de failure modes, timeouts, retries, exponential backoff, jitter, idempotency keys, duplicate requests, circuit breakers y dependencias externas.
2. ¿Qué garantía ofrece la solución principal y qué caso límite deja sin resolver?
3. Compara dos alternativas del tema y justifica cuándo elegirías cada una.

## Diseño

4. Diseña cómo aplicarías el tema a production-api-lab sin mezclar responsabilidades entre API, persistencia y operación.
5. Define una métrica, restricción o contrato que permita comprobar que tu diseño se comporta como esperas.

## Diagnóstico

6. Un comportamiento del laboratorio no coincide con la hipótesis. Propón observaciones, comandos o pruebas para aislar la causa antes de cambiar código.

## Implementación práctica

7. Implementa el escenario mínimo del laboratorio **LAB-BACKEND-009-idempotency-key** y registra resultado esperado frente a resultado real.
8. Rompe o estresa el escenario de forma controlada, aplica una solución y vuelve a medir.

## Experimento crítico de idempotencia

- Envía varias veces `POST /payments` con la misma cabecera `Idempotency-Key: example-key` y demuestra que existe un único efecto lógico.
- Repite con una clave distinta y con un cuerpo distinto para la misma clave; define el contrato de conflicto.
- Simula pérdida de respuesta y timeout entre cliente y servidor, y explica qué debe devolver un retry seguro.

## Decisión técnica

9. Escribe una recomendación breve con contexto, opciones, trade-offs, decisión provisional y cómo la verificarías. No la conviertas en ADR hasta que exista una decisión real aceptada.
