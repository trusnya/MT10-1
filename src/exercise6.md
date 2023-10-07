## Задание:

Перейдите на сайт https://www.w3schools.com/sql/trysql.asp?filename=trysql_op_in , который был создан как раз для обучения SQL-запросам. Прикрепите SQL команды, описания полученных результатов и скриншоты таблиц, которые выдаёт сервис после совершения запросов к БД. Причём на каждую таблицу (они расположены в правой части сайта) необходимо будет сделать по три запроса, один из которых должен быть сложным (содержать по 4-5 операторов запроса).

## Выполнение:

**Юлия**

## Таблица Customers:

1. SQL: SELECT * FROM Customers;

Описание результата: Возвращает все записи из таблицы Customers.

Скриншот Customers1

2.  SQL: SELECT * FROM Customers WHERE Country='Germany';

Описание результата: Возвращает все записи из таблицы Customers, где значение поля Country равно 'Germany'.

Скриншот Customers2

3. SQL: SELECT * FROM Customers WHERE City='London' AND ContactName LIKE '%Thomas%';

Описание результата: Возвращает все записи из таблицы Customers, где значение поля City равно 'London' и значение поля ContactName содержит строку 'Thomas'.

Скриншот Customers3

## Таблица Categories:

1. SQL:

Описание результата:

Скриншот

2. SQL:

Описание результата:

Скриншот

3. SQL:

Описание результата:

Скриншот

## Таблица Employees:

1. SQL:

Описание результата:

Скриншот

2. SQL:

Описание результата:

Скриншот

3. SQL:

Описание результата:

Скриншот

## Таблица OrderDetails:

1. SQL: SELECT * FROM OrderDetails;

Описание результата: Возвращает все записи из таблицы OrderDetails.

Скриншот OrderDetails1

2. SQL: SELECT * FROM OrderDetails WHERE Quantity>50;

Описание результата: Возвращает все записи из таблицы OrderDetails, где значение поля Quantity больше 50.

Скриншот OrderDetails2

3. SQL: SELECT * FROM OrderDetails WHERE OrderID>10400 AND Quantity>=10 ORDER BY ProductID ASC;

Описание результата: Возвращает все записи из таблицы OrderDetails, где значение поля OrderID больше 10400 и значение поля Quantity больше или равно 10, отсортированные по возрастанию поля ProductID.

Скриншот OrderDetails3

## Таблица Orders:

1. SQL: SELECT * FROM Orders;

Описание результата: Возвращает все записи из таблицы Orders.

Скриншот Orders1

2. SQL: SELECT * FROM Orders WHERE OrderDate='1996-07-15' OR OrderDate='1996-07-16';

Описание результата: Возвращает все записи из таблицы Orders, где значение поля OrderDate равно '1996-07-15' или '1996-07-16'.

Скриншот Orders2

3. SQL: SELECT * FROM Orders WHERE ShipperID='2' AND (EmployeeID='3' OR EmployeeID='5');

Описание результата: Возвращает все записи из таблицы Orders, где значение поля ShipperID равно '2' и значение поля EmployeeID равно '3' или '5'.

Скриншот Orders3

## Таблица Products:

1. SQL:

Описание результата:

Скриншот

2. SQL:

Описание результата:

Скриншот

3. SQL:

Описание результата:

Скриншот

## Таблица Shippers:

1. SQL:

Описание результата:

Скриншот

2. SQL:

Описание результата:

Скриншот

3. SQL:

Описание результата:

Скриншот

## Таблица Suppliers:

1. SQL:

Описание результата:

Скриншот

2. SQL:

Описание результата:

Скриншот

3. SQL:

Описание результата:

Скриншот