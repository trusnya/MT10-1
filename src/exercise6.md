## Таблица Customers:

1. 
```
SELECT * FROM Customers;
```

Описание результата: Возвращает все записи из таблицы Customers.

![Скриншот Customers1](https://repos.21-school.ru/students/MT10.ID_1261488/Team__TL__siskoari_student.21_school.ru_.yU_riUIJSrSKka9sbo9uAA/MT10-1/-/raw/develop/src/Materials/Customers1.png)

2. 
```
SELECT * FROM Customers WHERE Country='Germany';
```

Описание результата: Возвращает все записи из таблицы Customers, где значение поля Country равно 'Germany'.

![Скриншот Customers2](https://repos.21-school.ru/students/MT10.ID_1261488/Team__TL__siskoari_student.21_school.ru_.yU_riUIJSrSKka9sbo9uAA/MT10-1/-/raw/develop/src/Materials/Customers2.png)

3. 
```
SELECT Customers.CustomerName, COUNT(*) AS TotalOrders
FROM Customers
JOIN Orders ON Customers.CustomerID = Orders.CustomerID
GROUP BY Customers.CustomerName
HAVING COUNT(*) > 5;
```

Описание результата: Объединяет таблицы Customers и Orders по полю CustomerID. Затем он группирует результаты по имени клиента и подсчитывает общее количество заказов для каждого клиента. Затем он выбирает только тех клиентов, у которых количество заказов больше 5.

![Скриншот Customers3](https://repos.21-school.ru/students/MT10.ID_1261488/Team__TL__siskoari_student.21_school.ru_.yU_riUIJSrSKka9sbo9uAA/MT10-1/-/raw/develop/src/Materials/Customers3.png)

## Таблица Categories:

1. 
```
SELECT * FROM Categories;
```

Описание результата: Извлекает все записи из таблицы Categories и выводит их на экран.

![Скриншот Categories1](https://repos.21-school.ru/students/MT10.ID_1261488/Team__TL__siskoari_student.21_school.ru_.yU_riUIJSrSKka9sbo9uAA/MT10-1/-/raw/develop/src/Materials/Categories1.png)

2. 
```
SELECT CategoryName, Description FROM Categories WHERE CategoryID = 3;
```

Описание результата: Извлекает название категории и описание для категории с ID равным 3.

![Скриншот Categories2](https://repos.21-school.ru/students/MT10.ID_1261488/Team__TL__siskoari_student.21_school.ru_.yU_riUIJSrSKka9sbo9uAA/MT10-1/-/raw/develop/src/Materials/Categories2.png)

3. 
```
SELECT CategoryName, COUNT(*) AS TotalProducts
FROM Categories
JOIN Products ON Categories.CategoryID = Products.CategoryID
GROUP BY CategoryName
HAVING COUNT(*) > 5;
```

Описание результата: Объединяет таблицы Categories и Products по полю CategoryID. Затем он группирует результаты по названию категории и подсчитывает общее количество продуктов в каждой категории. Затем он выбирает только те категории, в которых количество продуктов больше 5.

![Скриншот Categories3](https://repos.21-school.ru/students/MT10.ID_1261488/Team__TL__siskoari_student.21_school.ru_.yU_riUIJSrSKka9sbo9uAA/MT10-1/-/raw/develop/src/Materials/Categories3.png)

## Таблица Employees:

1. 
```
SELECT * FROM Employees;
```

Описание результата: Выбирает все данные из таблицы Employees, включая все столбцы и строки.

![Скриншот Employees1](https://repos.21-school.ru/students/MT10.ID_1261488/Team__TL__siskoari_student.21_school.ru_.yU_riUIJSrSKka9sbo9uAA/MT10-1/-/raw/develop/src/Materials/Employees1.png)

2. 
```
SELECT FirstName, LastName, BirthDate FROM Employees ORDER BY BirthDate;
```

Описание результата: Выбирает имена и фамилии сотрудников, а также дату рождения и сортирует их по дате рождения.

![Скриншот Employees2](https://repos.21-school.ru/students/MT10.ID_1261488/Team__TL__siskoari_student.21_school.ru_.yU_riUIJSrSKka9sbo9uAA/MT10-1/-/raw/develop/src/Materials/Employees2.png)

3. 
```
SELECT Orders.OrderID, Customers.CustomerName, Employees.FirstName, Employees.LastName
FROM Orders
JOIN Customers ON Orders.CustomerID = Customers.CustomerID
JOIN Employees ON Orders.EmployeeID = Employees.EmployeeID
WHERE Customers.Country = 'Germany';
```

Описание результата: Выбирает идентификатор заказа, имя клиента, а также имя и фамилию сотрудника для заказов, где клиент из Германии. Он объединяет таблицы Orders, Customers и Employees по соответствующим полям CustomerID и EmployeeID.

![Скриншот Employees3](https://repos.21-school.ru/students/MT10.ID_1261488/Team__TL__siskoari_student.21_school.ru_.yU_riUIJSrSKka9sbo9uAA/MT10-1/-/raw/develop/src/Materials/Employees3.png)

## Таблица OrderDetails:

1. 
```
SELECT * FROM OrderDetails;
```

Описание результата: Возвращает все записи из таблицы OrderDetails.

![Скриншот OrderDetails1](https://repos.21-school.ru/students/MT10.ID_1261488/Team__TL__siskoari_student.21_school.ru_.yU_riUIJSrSKka9sbo9uAA/MT10-1/-/raw/develop/src/Materials/OrderDetails1.png)

2. 
```
SELECT * FROM OrderDetails WHERE Quantity>50;
```

Описание результата: Возвращает все записи из таблицы OrderDetails, где значение поля Quantity больше 50.

![Скриншот OrderDetails2](https://repos.21-school.ru/students/MT10.ID_1261488/Team__TL__siskoari_student.21_school.ru_.yU_riUIJSrSKka9sbo9uAA/MT10-1/-/raw/develop/src/Materials/OrderDetails2.png)

3. 
```
SELECT OrderID, ProductID, Quantity, OrderDetailID
FROM OrderDetails
WHERE Quantity > 10
ORDER BY OrderDetailID DESC;
```

Описание результата: Bыбирает поля OrderID, ProductID, Quantity и OrderDetailID из таблицы OrderDetails. Затем она фильтрует только те строки, где значение поля Quantity больше 10. Наконец, она сортирует результаты по убыванию значения поля OrderDetailID.

![Скриншот OrderDetails3](https://repos.21-school.ru/students/MT10.ID_1261488/Team__TL__siskoari_student.21_school.ru_.yU_riUIJSrSKka9sbo9uAA/MT10-1/-/raw/develop/src/Materials/OrderDetails3.png)

## Таблица Orders:

1. 
```
SELECT * FROM Orders;
```

Описание результата: Возвращает все записи из таблицы Orders.

![Скриншот Orders1](https://repos.21-school.ru/students/MT10.ID_1261488/Team__TL__siskoari_student.21_school.ru_.yU_riUIJSrSKka9sbo9uAA/MT10-1/-/raw/develop/src/Materials/Orders1.png)

2. 
```
SELECT * FROM Orders WHERE OrderDate='1996-07-15' OR OrderDate='1996-07-16';
```

Описание результата: Возвращает все записи из таблицы Orders, где значение поля OrderDate равно '1996-07-15' или '1996-07-16'.

![Скриншот Orders2](https://repos.21-school.ru/students/MT10.ID_1261488/Team__TL__siskoari_student.21_school.ru_.yU_riUIJSrSKka9sbo9uAA/MT10-1/-/raw/develop/src/Materials/Orders2.png)

3. 
```
SELECT Orders.OrderID, Customers.CustomerID, Employees.EmployeeID, Orders.OrderDate, Shippers.ShipperID
FROM Orders
INNER JOIN Customers ON Orders.CustomerID = Customers.CustomerID
INNER JOIN Employees ON Orders.EmployeeID = Employees.EmployeeID
INNER JOIN Shippers ON Orders.ShipperID = Shippers.ShipperID;
```

Описание результата: Объединяет таблицы "Orders", "Customers", "Employees" и "Shippers" по соответствующим идентификаторам (CustomerID, EmployeeID, ShipperID). В результате выполнения команды будут выбраны столбцы OrderID, CustomerID, EmployeeID, OrderDate и ShipperID из таблиц Orders, Customers, Employees и Shippers соответственно.

![Скриншот Orders3](https://repos.21-school.ru/students/MT10.ID_1261488/Team__TL__siskoari_student.21_school.ru_.yU_riUIJSrSKka9sbo9uAA/MT10-1/-/raw/develop/src/Materials/Orders3.png)

## Таблица Products:

1. 
```
SELECT * FROM Products;
```

Описание результата: Возвращает все записи из таблицы Products.

![Скриншот Products1](https://repos.21-school.ru/students/MT10.ID_1261488/Team__TL__siskoari_student.21_school.ru_.yU_riUIJSrSKka9sbo9uAA/MT10-1/-/raw/develop/src/Materials/Products1.png)

2. 
```
SELECT * FROM Products WHERE Price < 10;
```

Описание результата: Возвращает все записи из таблицы Products, где значение поля Price меньше '10'

![Скриншот Products2](https://repos.21-school.ru/students/MT10.ID_1261488/Team__TL__siskoari_student.21_school.ru_.yU_riUIJSrSKka9sbo9uAA/MT10-1/-/raw/develop/src/Materials/Products2.png)

3. 
```
SELECT ProductName, Price FROM Products 
WHERE Price < 10 AND ProductName LIKE 'F%' 
AND ProductID NOT IN (4,6) 
ORDER BY Price DESC;
```

Описание результата: Будет выведена таблица со всеми продуктами, у которых цена меньше 10, имена которых начинаются на "F", исключая продукты с ProductID 4 и 6. Результат отсортирован по цене по убыванию и содержит только названия продуктов и их цены.

![Скриншот Products3](https://repos.21-school.ru/students/MT10.ID_1261488/Team__TL__siskoari_student.21_school.ru_.yU_riUIJSrSKka9sbo9uAA/MT10-1/-/raw/develop/src/Materials/Products3.png)

## Таблица Shippers:

1. 
```
SELECT * FROM Shippers;
```

Описание результата: Возвращает все записи из таблицы Shippers.

![Скриншот Shippers1](https://repos.21-school.ru/students/MT10.ID_1261488/Team__TL__siskoari_student.21_school.ru_.yU_riUIJSrSKka9sbo9uAA/MT10-1/-/raw/develop/src/Materials/Shippers1.png)

2. 
```
SELECT * FROM Shippers 
WHERE ShipperID = 1;
```

Описание результата: Возвращает все записи из таблицы Shippers, где значение поля ShipperID равно '1'.

![Скриншот Shippers2](https://repos.21-school.ru/students/MT10.ID_1261488/Team__TL__siskoari_student.21_school.ru_.yU_riUIJSrSKka9sbo9uAA/MT10-1/-/raw/develop/src/Materials/Shippers2.png)

3. 
```
JOIN Shippers ON Orders.ShipperID = Shippers.ShipperID 
JOIN OrderDetails ON Orders.OrderID = OrderDetails.OrderID 
WHERE OrderDetails.Quantity > 5 AND Shippers.ShipperName = 'Federal Shipping' 
GROUP BY Orders.OrderID 
ORDER BY Orders.OrderDate ASC;
```

Описание результата: Будет выведена таблица со всеми заказами, которые содержали более 5 единиц товара, и были доставлены компанией "Federal Shipping". Результат отсортирован по дате заказа по возрастанию и содержит номер заказа, дату заказа, название компании-доставщика и общее количество заказанных единиц.

![Скриншот Shippers3](https://repos.21-school.ru/students/MT10.ID_1261488/Team__TL__siskoari_student.21_school.ru_.yU_riUIJSrSKka9sbo9uAA/MT10-1/-/raw/develop/src/Materials/Shippers3.png)

## Таблица Suppliers:

1. 
```
SELECT * FROM Suppliers;
```

Описание результата: Возвращает все записи из таблицы Suppliers.

![Скриншот Suppliers1](https://repos.21-school.ru/students/MT10.ID_1261488/Team__TL__siskoari_student.21_school.ru_.yU_riUIJSrSKka9sbo9uAA/MT10-1/-/raw/develop/src/Materials/Suppliers1.png)

2. 
```
SELECT * FROM Suppliers WHERE Country = 'Germany';
```

Описание результата: Возвращает все записи из таблицы Suppliers, где значение поля Country равно 'Germany'.

![Скриншот Suppliers2](https://repos.21-school.ru/students/MT10.ID_1261488/Team__TL__siskoari_student.21_school.ru_.yU_riUIJSrSKka9sbo9uAA/MT10-1/-/raw/develop/src/Materials/Suppliers2.png)

3. 
```
SELECT Suppliers.SupplierName, AVG(Products.Price) AS AveragePrice 
FROM Suppliers 
JOIN Products ON Suppliers.SupplierID = Products.SupplierID 
GROUP BY Suppliers.SupplierName 
HAVING AVG(Products.Price) > 20 
ORDER BY AveragePrice DESC;
```

Описание результата: Будет выведена таблица со всеми поставщиками, у которых есть продукты в таблице Products, и средняя цена продуктов, которые они поставляют, выше 20. Результат отсортирован по убыванию средней цены и содержит название поставщика и среднюю цену продуктов.

![Скриншот Suppliers3](https://repos.21-school.ru/students/MT10.ID_1261488/Team__TL__siskoari_student.21_school.ru_.yU_riUIJSrSKka9sbo9uAA/MT10-1/-/raw/develop/src/Materials/Suppliers3.png)