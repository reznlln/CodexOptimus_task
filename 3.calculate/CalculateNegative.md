**Описание**

Негативные проверки метода:
POST /api/discount/calculate

Этот метод принимает количество баллов в качестве параметра и возвращает процент скидки в соответствии с условиями начисления.

Правила расчета скидки:

- От 0 до 150 баллов - скидка 1%
- От 150 до 200 баллов - скидка 5%
- От 200 до 400 баллов - скидка 7%
- От 400 баллов - скидка 10%


* [x] **Case_1:**
      
Request: -100

Response: 400 Error с сообщением об ошибке при недопустимых входных данных.

* [x] **Case_2:** //Отправляем не целое число, т.к клиенту начисляются по 1 баллу за каждые 1000 рублей
      
Request: 4.5

Response: 400 Error с сообщением об ошибке при недопустимых входных данных.

* [x] **Case_3:**
      
Request: abc

Response: 400 Error с сообщением об ошибке при недопустимых входных данных.

* [x] **Case_4:**
      
Request: 14!

Response: 400 Error с сообщением об ошибке при недопустимых входных данных.


* [x] **Case_5:** //Тест безопасности

Request: {"points": "400 OR 1=1"}

Response: 400 Error с сообщением об ошибке при недопустимых входных данных.


* [x] **Case_6:**
      
Header: Accept-Language: "language"

Request: -100

Response: 400 Error с сообщением об ошибке при недопустимых входных данных на языке указанном в параметре "language" при наличие локализации ошибок.

