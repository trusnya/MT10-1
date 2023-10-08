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

3. SQL: SELECT Customers.CustomerName, COUNT(*) AS TotalOrders
FROM Customers
JOIN Orders ON Customers.CustomerID = Orders.CustomerID
GROUP BY Customers.CustomerName
HAVING COUNT(*) > 5;

Описание результата: Объединяет таблицы Customers и Orders по полю CustomerID. Затем он группирует результаты по имени клиента и подсчитывает общее количество заказов для каждого клиента. Затем он выбирает только тех клиентов, у которых количество заказов больше 5.

Скриншот Customers3

## Таблица Categories:

1. SQL: SELECT * FROM Categories;

Описание результата: Извлекает все записи из таблицы Categories и выводит их на экран.

Скриншот Categories1

2. SQL: SELECT CategoryName, Description FROM Categories WHERE CategoryID = 3;

Описание результата: Извлекает название категории и описание для категории с ID равным 3.

Скриншот Categories2

3. SQL: SELECT CategoryName, COUNT(*) AS TotalProducts
FROM Categories
JOIN Products ON Categories.CategoryID = Products.CategoryID
GROUP BY CategoryName
HAVING COUNT(*) > 5;

Описание результата: Объединяет таблицы Categories и Products по полю CategoryID. Затем он группирует результаты по названию категории и подсчитывает общее количество продуктов в каждой категории. Затем он выбирает только те категории, в которых количество продуктов больше 5.

Скриншот Categories3

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

3. SQL:

Описание результата:

Скриншот OrderDetails3

## Таблица Orders:

1. SQL: SELECT * FROM Orders;

Описание результата: Возвращает все записи из таблицы Orders.

Скриншот Orders1

2. SQL: SELECT * FROM Orders WHERE OrderDate='1996-07-15' OR OrderDate='1996-07-16';

Описание результата: Возвращает все записи из таблицы Orders, где значение поля OrderDate равно '1996-07-15' или '1996-07-16'.

Скриншот Orders2

3. SQL: 

Описание результата: 

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