SQL Exercises
=============

Part i
======

1.
==

SELECT \* FROM Customers WHERE Country = 'UK';

2.
==

SELECT CustomerName From Customers LEFT JOIN Orders ON
Customers.CustomerID = Orders.CustomerID GROUP BY Customers.CustomerID
ORDER BY COUNT(OrderID) DESC LIMIT 1;

3
=

SELECT SupplierName From Suppliers LEFT JOIN Products ON
Suppliers.SupplierID = Products.SupplierID GROUP BY Suppliers.SupplierID
ORDER BY AVG(Price) DESC LIMIT 1;

4
=

SELECT COUNT(DISTINCT(COUNTRY)) As Num\_Distinct\_Countries FROM
Customers;

5
=

SELECT Categories.CategoryName From Products LEFT JOIN OrderDetails ON
Products.ProductID = OrderDetails.ProductID LEFT JOIN Categories ON
Categories.CategoryID = Products.CategoryID GROUP BY Products.CategoryID
ORDER BY COUNT(Distinct(OrderID)) DESC LIMIT 1;

6
=

SELECT SUM(Quantity \* Price) From OrderDetails LEFT JOIN Products ON
OrderDetails.ProductID = Products.ProductID GROUP BY OrderID ORDER BY
Sum(Quantity \* Price) DESC LIMIT 10;

7
=

SELECT Employees.LastName, Employees.FirstName, ROUND(Sum(Price \*
Quantity)) as Total\_Sales From Employees LEFT JOIN Orders ON
Orders.EmployeeID = Employees.EmployeeID LEFT JOIN OrderDetails ON
Orders.OrderID = OrderDetails.OrderID LEFT JOIN Products ON
OrderDetails.ProductID = Products.ProductID GROUP BY Employees.LastName,
Employees.FirstName ORDER BY ROUND(Sum(Price \* Quantity)) DESC LIMIT 1;

8
=

SELECT \* FROM Employees WHERE Notes LIKE "%BS%" LIMIT 10 ;

9
=

SELECT SupplierName From Suppliers LEFT JOIN Products ON
Suppliers.SupplierID = Products.SupplierID GROUP BY Suppliers.SupplierID
HAVING COUNT(ProductID) \> 2 ORDER BY AVG(Price) DESC LIMIT 1;
