**Описание:**
Проверка начисления бонусных баллов.
За каждые 1000 рублей потраченные клиентом начисляется 1 балл. 
В ответе возвращает обновленное количество бонусных баллов клиента.

<!-- TODO-IST:START -->
*[ ] Case_1

Request: /client_1/purchase
Body: Sum:999
Response: Count:0

*[ ] Case_2

Request: /client_1/purchase
Body: 1000
Response: Count:1

*[ ] Case_3

Request: /client_1/purchase
Body: 1001
Response: Count:2

* [ ] Case_4

Request: /client_1/purchase
Body: 2000
Response: Count:4
<!-- TODO-IST:END -->
