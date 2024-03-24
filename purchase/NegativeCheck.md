**Негативные проверки**

POST /api/customer/{customer_id}/purchase

Ввод невалидных значений, метод возвращает 4** ошибку

* [x] **Case_1**
      
Request: /client_1/purchase

Body: {value}

Response: 400 Error

где {value}:

	- test
	- null
	- 12!@#

* [x] **Case_2**
      
Request: /{client}/purchase

Body: 1000

Response: 400 Error

где {client}:

	- id несуществующего клиента в системе
 	- null

  * [x] **Case_3**
        
Вопрос, как называется параметр, в котором отправляем сумму покупки?
В данном тесте отправить наименование параметра в теле запроса, которое не соответствует требованию. И убедиться, что есть ошибка.
