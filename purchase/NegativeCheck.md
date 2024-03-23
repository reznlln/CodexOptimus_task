**Негативные проверки**

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
