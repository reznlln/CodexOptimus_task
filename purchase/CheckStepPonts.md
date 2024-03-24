**Описание:**

POST /api/customer/{customer_id}/purchase

Позитивные проверки.
- Проверка начисления бонусных баллов.
- За каждые 1000 рублей потраченные клиентом начисляется 1 балл. 
- В ответе возвращает обновленное количество бонусных баллов клиента.

В системе существует клиент с id client_1.

<!-- TODO-IST:START -->
* [x] **Case_1**

Request: /client_1/purchase

Body: 999

Response: 0

* [x] **Case_2**

Request: /client_1/purchase

Body: 1000

Response: 1

* [x] **Case_3**

Request: /client_1/purchase

Body: 1001

Response: 2

* [x] **Case_4**

Request: /client_1/purchase

Body: 2000

Response: 4

* [x] **Case_5**

Request: /client_1/purchase

Body: 0

Response: 4

* [x] **Case_6**
      
Проверить соответствие наименований входного и выходного параметра при наличии.

* [x] **Case_7**
      
Проверить локализацию сообщений при наличие в методе. В Header отправить Accept-Language: "language"
