# Заказы
## order
- `id` - integer - технический id
- `order_id` - integer - основной id
- `site_id` - integer - сайт
- `order_type` - integer - тип заказа
- `user_id` - integer - id пользователя
- `status_id` - integer - id статус заказа
- `delivery_id` - integer - id доставки
- `adress_id` - integer - адрес доставки
- `conditions_id` - integer - id контракта
- `seller_id` - integer - id продавца
- `state` - integer - статус
- `alias` - string - алиас
- `score` - integer - количество запросов
### `order` schema - структура таблицы
```json
{
"order_id": "integer",
"site_id": "integer",
"order_type": "integer",
"user_id": "integer",
"status_id": "integer",
"delivery_id": "integer",
"adress_id": "integer",
"conditions_id": "integer",
"seller_id": "integer",
"state": "integer",
"alias": "string",
"score": "integer"
}
```
### `order` relations - связи
```json
"relations": {
 "user": {
  "type": "belongsTo",
  "keys": {
   "local": "user_id",
   "foreign": "order_id"
  }
 }
}
```
