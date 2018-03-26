## 595.Big Countries 

 - url: [https://leetcode.com/problems/big-countries/description/][1]
 - analysis:
 - solution:
 
```MySQL
SELECT name, population, area
FROM World
WHERE population>25000000 OR area>3000000
```


----------
## 627.Swap Salary

 - url:
 - analysis:
 - solution:
 
 ```MySQL
 UPDATE salary
 SET sex = (CASE when sex = 'm'
            THEN 'f'
            ELSE 'm'
            END) 
```



----------
## 192.Duplicate Emails

 - url:
 - analysis:
 - solution:
 
 ```MySQL
 SELECT Email
 FROM Person
 GROUP BY Email
 HAVING count(*) > 1

```

----------
## 175.Combine Two Tables

 - url:
 - analysis: 不同表的联结，过滤条件应使用ON而不用，但用法一样
 - solution:
 
 ```MySQL
SELECT FirstName, LastName, City, State
FROM Person LEFT JOIN Address
ON Person.PersonId=Address.PersonId
```
----------
## 181.Employees Earning More Than Their Managers

 - url:
 - analysis: 
 - solution:
 
```MySQL

SELECT E1.Employee AS Employee
FROM Employee AS E1 INNER  Employee AS E2
ON E1.ManagerId = E2.Id AND E1.Salary > E2.Salary


``` 
 
 ```MySQL
SELECT Name AS Employee
FROM Employee AS E1
WHERE Salary > (SELECT Salary
                FROM Employee AS E2
                WHERE E1.ManagerId=E2.Id)
```
 
 
----------
## 183.Customers Who Never Order 

 - url:
 - analysis: 
 - solution:
 
 ```MySQL
SELECT Name AS Customers
FROM Customers RIGHT JOIN Orders
ON Customers.Id = Orders.CustomerId
WHERE Orders.Id IS NULL
```
------------
## 197.Rising Temperature

 - url:
 - analysis: 
 - solution:
 
 ```MySQL
SELECT W1.Id
FROM Weather AS W1, Weather AS W2
ON TO_DAYS(W1.Date)=TO_DAYS(W2.Date)+1 AND W1.Temperature>W2.Temperature
```
-----------

## 184.Department Highest Salary

 - url:
 - analysis:
 - solution:
 
 ```MySQL
SELECT D.Name AS Department, E.Name AS Employee, E.Salary AS Salary
FROM Employee AS E, Department AS D
WHERE E.Department = D.Id
AND E.Salary = (SELECT MAX(Salary)
                FROM Employee AS E2
                WHERE E2.DepartmentId = D.Id)
``` 
 
-------------     
## 176.Second Highest Salary

 - url:
 - analysis:
 - solution:
 
 ```MySQL

``` 
 
 
-------------     
## 180.Consecutive Numbers

 - url:
 - analysis:
 - solution:
-------------     
## 196.Delete Duplicate Emails

 - url:
 - analysis:
 - solution:
-------------     
## 
 
 
 
 
 
  [1]: https://leetcode.com/problems/big-countries/description/