**Описание**

Позитивные проверки метода. 
Возвращаемый процент скидки соответствует ожидаемому значению в соответствии с условиями начисления.
POST /api/discount/calculate

Правила расчета скидки:

- От 0 до 150 баллов - скидка 1%
- От 150 до 200 баллов - скидка 5%
- От 200 до 400 баллов - скидка 7%
- От 400 баллов - скидка 10%

НЕ ТОЧНЫЕ требования, т.к крайние значения попадают сразу в два диапазона.

Допустим для примера взяли крайние значения 149, 199 и 399 баллов соответственно для 1%, 5% и 7% скидки.

* [x] **Case_1:**
      
Request: 0

Response: 1

* [x] **Case_2:**
      
Request: 149

Response: 1

* [x] **Case_3:**
      
Request: 150

Response: 5

* [x] **Case_4:**
      
Request: 199

Response: 5

* [x] **Case_5:**
      
Request: 200

Response: 7

* [x] **Case_6:**
      
Request: 399

Response: 7

* [x] **Case_7:**
      
Request: 400

Response: 10

* [x] **Case_8:**
      
Request: 10000

Response: 10

* [x] **Case_9:**
      
Request: 47383940505050

Response: 10

* [x] **Case_10:**
Проверить соответствие наименований входного и выходного параметра при наличии.
