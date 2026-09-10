# Preguntas de recuperación — Sesión 06

## Fundamentales

- Explica el flujo completo de **Transactions & Concurrency** sin usar definiciones memorizadas.
- ¿Qué invariantes o garantías son importantes y qué observación las demostraría?
- ¿Qué parte del modelo suele ocultar una abstracción de framework?

## Producción

- ¿Qué cambiaría bajo carga, concurrencia, fallos parciales o despliegues múltiples?
- ¿Qué contrato, métrica o alerta protegería a los usuarios?
- ¿Cómo evolucionaría la solución sin romper clientes o datos existentes?

## Diagnóstico

- El laboratorio produce un resultado inesperado. ¿Qué medirías primero y por qué?
- ¿Qué evidencia distinguiría un problema de aplicación, base de datos, red o configuración?
- ¿Qué rollback sería seguro y cómo confirmarías que el problema no reaparece?

## Trade-offs

- Compara simplicidad, coste, latencia, consistencia y operabilidad de dos enfoques.
- ¿Qué garantía estás sacrificando o comprando con tu elección?
- ¿En qué contexto dejarías de usar tu solución actual?

## Entrevista técnica

- Diseña una respuesta defendible para un caso de producción relacionado con **Transactions & Concurrency**.
- Una solución funciona en desarrollo pero falla en producción. ¿Qué hipótesis priorizas?
- Explica una decisión a una persona que cuestiona tu diseño y responde a una objeción concreta.
