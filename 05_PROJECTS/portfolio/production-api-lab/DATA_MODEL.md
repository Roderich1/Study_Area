# Modelo de datos

Estado: `PLANNED`.

## Entidades candidatas

`users`, `products`, `inventory`, `orders`, `order_items`, `payments`.

Se deberán definir PK, FK, `UNIQUE`, `CHECK`, `NOT NULL`, cardinalidades, invariantes de stock y claves de idempotencia antes de implementar migraciones. No se declara todavía un esquema final ni una migración aplicada.

## Preguntas de diseño

- ¿Qué invariantes deben vivir en PostgreSQL?
- ¿Cómo se evita vender stock dos veces?
- ¿Cómo se relaciona un pago repetido con su `Idempotency-Key`?
- ¿Qué datos necesitan historial o auditoría?
