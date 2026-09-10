# Ejercicios — Sesión 11

Intenta resolverlos antes de consultar soluciones. Registra razonamiento, supuestos y evidencia; las respuestas no se proporcionan automáticamente.

## Comprensión

1. Explica con un diagrama cómo se relacionan los conceptos de caching, cache-aside, TTL, invalidation, cache stampede, stale data, distributed cache, Redis, sessions y rate limiting.
2. ¿Qué garantía ofrece la solución principal y qué caso límite deja sin resolver?
3. Compara dos alternativas del tema y justifica cuándo elegirías cada una.

## Diseño

4. Diseña cómo aplicarías el tema a production-api-lab sin mezclar responsabilidades entre API, persistencia y operación.
5. Define una métrica, restricción o contrato que permita comprobar que tu diseño se comporta como esperas.

## Diagnóstico

6. Un comportamiento del laboratorio no coincide con la hipótesis. Propón observaciones, comandos o pruebas para aislar la causa antes de cambiar código.

## Implementación práctica

7. Implementa el escenario mínimo del laboratorio **LAB-BACKEND-010-redis-cache** y registra resultado esperado frente a resultado real.
8. Rompe o estresa el escenario de forma controlada, aplica una solución y vuelve a medir.

## Medición obligatoria

- Mide latencia y consultas antes de activar la caché.
- Activa cache-aside con TTL, repite la medición y conserva los datos observados.
- Invalida o modifica el recurso, demuestra el comportamiento de datos stale y justifica la política de invalidación.

## Decisión técnica

9. Escribe una recomendación breve con contexto, opciones, trade-offs, decisión provisional y cómo la verificarías. No la conviertas en ADR hasta que exista una decisión real aceptada.
