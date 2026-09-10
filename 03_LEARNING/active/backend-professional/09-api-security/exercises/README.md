# Ejercicios — Sesión 09

Intenta resolverlos antes de consultar soluciones. Registra razonamiento, supuestos y evidencia; las respuestas no se proporcionan automáticamente.

## Comprensión

1. Explica con un diagrama cómo se relacionan los conceptos de OWASP API Security, BOLA/IDOR, broken authentication, property authorization, mass assignment, SQL injection, SSRF, CORS, CSRF, rate limiting, secrets, password hashing, headers, least privilege y threat modeling.
2. ¿Qué garantía ofrece la solución principal y qué caso límite deja sin resolver?
3. Compara dos alternativas del tema y justifica cuándo elegirías cada una.

## Diseño

4. Diseña cómo aplicarías el tema a production-api-lab sin mezclar responsabilidades entre API, persistencia y operación.
5. Define una métrica, restricción o contrato que permita comprobar que tu diseño se comporta como esperas.

## Diagnóstico

6. Un comportamiento del laboratorio no coincide con la hipótesis. Propón observaciones, comandos o pruebas para aislar la causa antes de cambiar código.

## Implementación práctica

7. Implementa el escenario mínimo del laboratorio **LAB-BACKEND-008-bola-authorization** y registra resultado esperado frente a resultado real.
8. Rompe o estresa el escenario de forma controlada, aplica una solución y vuelve a medir.

## Ataque controlado

- Crea dos identidades de prueba y ejecuta contra datos propios una solicitud BOLA/IDOR que cambie el identificador del recurso.
- Registra la respuesta vulnerable solo en evidencias locales sin secretos, explica la autorización que faltó y aplica la mitigación.
- Repite la solicitud después del cambio y demuestra que el acceso legítimo sigue funcionando.

## Decisión técnica

9. Escribe una recomendación breve con contexto, opciones, trade-offs, decisión provisional y cómo la verificarías. No la conviertas en ADR hasta que exista una decisión real aceptada.
