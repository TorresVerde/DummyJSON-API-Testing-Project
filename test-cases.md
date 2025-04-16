# 🧪 Тест-кейсы для DummyJSON API (/products)

## TC001: Получение списка продуктов
- Метод: GET
- Endpoint: /products
- Ожидаемый результат: 200 OK, поле "products" содержит массив

## TC002: Получение продукта по ID
- Метод: GET
- Endpoint: /products/1
- Ожидаемый результат: 200 OK, "id": 1

## TC003: Создание нового продукта
- Метод: POST
- Endpoint: /products/add
- Body:
  {
    "title": "TestProduct",
    "price": 1000
  }
- Ожидаемый результат: 200 OK, "title": "TestProduct", "id" существует

## TC004: Обновление цены продукта
- Метод: PUT
- Endpoint: /products/1
- Body:
  {
    "price": 888
  }
- Ожидаемый результат: 200 OK, "price": 888

## TC005: Удаление продукта
- Метод: DELETE
- Endpoint: /products/1
- Ожидаемый результат: 200 OK, "isDeleted": true

## TC006: Попытка получить несуществующий продукт
- Метод: GET
- Endpoint: /products/99999
- Ожидаемый результат: 404 Not Found
