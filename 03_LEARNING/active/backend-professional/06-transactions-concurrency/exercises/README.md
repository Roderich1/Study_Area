# Ejercicios — Sesión 06

Intenta resolverlos antes de consultar soluciones. Registra razonamiento, supuestos y evidencia; las respuestas no se proporcionan automáticamente.

## Comprensión

1. Explica con un diagrama cómo se relacionan los conceptos de ACID, transactions, MVCC, isolation levels, Read Committed, Repeatable Read, Serializable, dirty/non-repeatable/phantom reads, lost updates, locks, deadlocks, race conditions y locking optimista/pesimista.
2. ¿Qué garantía ofrece la solución principal y qué caso límite deja sin resolver?
3. Compara dos alternativas del tema y justifica cuándo elegirías cada una.

## Diseño

4. Diseña cómo aplicarías el tema a production-api-lab sin mezclar responsabilidades entre API, persistencia y operación.
5. Define una métrica, restricción o contrato que permita comprobar que tu diseño se comporta como esperas.

## Diagnóstico

6. Un comportamiento del laboratorio no coincide con la hipótesis. Propón observaciones, comandos o pruebas para aislar la causa antes de cambiar código.

## Implementación práctica

7. Implementa el escenario mínimo del laboratorio **LAB-BACKEND-005-lost-update** y registra resultado esperado frente a resultado real.
8. Rompe o estresa el escenario de forma controlada, aplica una solución y vuelve a medir.

## Experimento crítico de concurrencia

- Configura `stock = 1` y lanza una compra desde request A y otra desde request B de forma concurrente.
- Reproduce primero la venta doble o el comportamiento incorrecto, captura la evidencia y explica la carrera.
- Implementa una solución con locking optimista o pesimista, repite el experimento y justifica el isolation level elegido.
- Diseña una variante que pueda producir deadlock y documenta el orden seguro de adquisición de locks.

## Decisión técnica

9. Escribe una recomendación breve con contexto, opciones, trade-offs, decisión provisional y cómo la verificarías. No la conviertas en ADR hasta que exista una decisión real aceptada.
