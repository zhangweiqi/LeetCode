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
  [1]: https://leetcode.com/problems/big-countries/description/