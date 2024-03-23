**Описание:**

GET /api/customer/{customer_id}/points
метод возвращает текущее количество бонусных баллов для указанного клиента.

Клиент client_3 не существует в системе.

* [x] **Case_1**

Request: GET /api/customer/client_3/points

Response: 400 Ошибка, с сообщением "Не найден клиент"
