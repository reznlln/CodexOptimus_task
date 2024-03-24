**Описание:**

GET /api/customer/{customer_id}/points

метод возвращает текущее количество бонусных баллов для указанного клиента.

В системе существую клиенты:

- client_1 = 5 баллов
- client_2 = 10 баллов

* [ ] **Case_1**

Request: GET /api/customer/client_1/points

Response: 5

* [ ] **Case_2**

Request: GET /api/customer/client_2/points

Response: 10

* [ ] **Case_3**

Для клиента client_1 обновить количество баллов = 150

Request: GET /api/customer/client_1/points

Response: 150
