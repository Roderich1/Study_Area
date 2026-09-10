# Sesión 04 — Relational Data Modeling

## Objetivo

Modelar datos relacionales con integridad explícita y migraciones reproducibles.

## Por qué importa en producción

proponer el modelo inicial de production-api-lab y una secuencia segura de migraciones. Un backend profesional debe hacer explícitos sus límites, fallos y costes; una implementación que funciona una vez no demuestra comportamiento seguro bajo carga, concurrencia o evolución.

## Prerrequisitos

Revisar las sesiones anteriores indicadas en el roadmap, tener Java 21+, Git, Linux, Docker y acceso a PostgreSQL disponibles, y leer el README de [production-api-lab](../../../../05_PROJECTS/portfolio/production-api-lab/README.md). No se requiere conocimiento consolidado previo del tema.

## Modelo mental

Problema real → concepto → trade-off → solución → implementación → experimento que puede fallar → explicación y documentación.

## Conceptos fundamentales

entities, relationships, PK, FK, UNIQUE, CHECK, NOT NULL, normalization, denormalization, integridad, schema evolution y Flyway.

## Agenda de 120 minutos

### 0–10 min — Active Recall

Sin consultar apuntes, escribir lo que se recuerda de las dependencias y formular dos hipótesis sobre el problema de esta sesión.

### 10–45 min — Teoría

Construir el modelo mental, contrastar alternativas y anotar qué garantías ofrece cada una y cuáles no.

### 45–95 min — Laboratorio

Implementar o instrumentar el escenario de [LAB-BACKEND-004-postgresql-query-plan](../../../../04_LABS/backend/LAB_INDEX.md#lab-backend-004-postgresql-query-plan) dentro de production-api-lab. Romperlo deliberadamente cuando sea seguro, observar la evidencia y registrar resultado esperado y real por separado.

### 95–105 min — Explicación sin apuntes

Explicar el flujo, una limitación y una decisión a otra persona o mediante una grabación/notas de voz. Escribir después las lagunas detectadas.

### 105–120 min — Revisión

Actualizar ejercicios, preguntas, errores reales, entregables y checkpoint. Si falta evidencia, dejar el módulo REVIEW_REQUIRED o BLOCKED, no inventar avance.

## Laboratorio asociado

**LAB-BACKEND-004-postgresql-query-plan** — proponer el modelo inicial de production-api-lab y una secuencia segura de migraciones. La planificación y el contrato del laboratorio están en [04_LABS/backend/LAB_INDEX.md](../../../../04_LABS/backend/LAB_INDEX.md).

## Ejercicios

Resolver primero los ejercicios de [exercises/README.md](exercises/README.md); después enlazar las decisiones o evidencias resultantes. Hay al menos tres preguntas conceptuales, dos ejercicios prácticos, un diagnóstico y una decisión técnica.

## Preguntas que debo poder responder

Usar [questions/questions.md](questions/questions.md) para recuperación activa. La respuesta debe explicar causas, garantías, límites y trade-offs, no repetir definiciones.

## Errores comunes

Consultar [mistakes/mistakes.md](mistakes/mistakes.md) solo después de intentar el laboratorio. Ese registro debe contener únicamente errores reales propios.

## Recursos recomendados

[PostgreSQL constraints](https://www.postgresql.org/docs/current/ddl-constraints.html) y [Flyway documentation](https://documentation.red-gate.com/flyway). Mantener la lista curada en [09_RESOURCES/backend-resources.md](../../../../09_RESOURCES/backend-resources.md).

## Entregables

- notas provisionales y preguntas actualizadas;
- ejercicios razonados;
- laboratorio planificado o ejecutado con evidencia real;
- cambio correspondiente, si procede, en production-api-lab;
- checkpoint autoevaluado y estado actualizado en progress.md.

## Criterio de finalización

Puedo explicar el modelo sin apuntes, aplicar el concepto en el proyecto, diagnosticar un fallo reproducible, justificar una alternativa y obtener promedio >= 4/5 en el checkpoint. Solo entonces el contenido puede considerarse candidato a consolidación.

## Qué puede consolidarse posteriormente en KNOWLEDGE

Después de estudiar y verificar, podrían promoverse explicaciones refinadas sobre entities, relationships, PK, FK, UNIQUE, CHECK, NOT NULL, normalization, denormalization, integridad, schema evolution y Flyway, separadas de los apuntes crudos. Este módulo no afirma que ese conocimiento ya esté consolidado.
