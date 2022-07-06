# SQL-advanced-queries

---
## MaTS
![meme](./images/meme.jpeg)

---
### About

In this assignment I'm diving deeper in the world of queries.  
I will be solving a *quiz* and put my answers to set quiz here.

---

### Solutions

1. 
```` 
SELECT COUNT(customerNumber) FROM customers 
````  
2. 
````
SELECT customerNumber FROM customers
WHERE contactFirstName='mary' AND contactLastName='young';
````  
3. 
````
SELECT customerNumber FROM customers
WHERE addressLine1='Magazinweg 7';
````
4. 
````
SELECT email FROM employees
ORDER BY lastName LIMIT 1;
````
5.
````
SELECT email FROM employees
ORDER BY lastName DESC LIMIT 1;   
````
6. 
````
SELECT productCode FROM products
WHERE productLine ='Trucks and Buses'
ORDER BY productScale, productName
LIMIT 1;  
````
7. 
````
SELECT email FROM employees
WHERE lastName LIKE 'T%'
ORDER BY lastName;  
````
8. 
````
SELECT customerNumber FROM payments
WHERE paymentDate = '2004-01-19';   
````
9. 
````
SELECT count(customerNumber) FROM customers
WHERE state = 'NV' OR state = 'NY';   
````
10.
````
SELECT count(customerNumber) FROM customers
WHERE state = 'NV' OR state = 'NY' OR country != 'usa';   
````
11.
````
SELECT COUNT(customerNumber) FROM customers
WHERE state = 'NV' OR state = 'NY' OR country != 'usa' AND creditLimit > 1000;
````
12.
````
SELECT COUNT(customerNumber) FROM customers
WHERE salesRepEmployeeNumber is null;   
````
13.
````
SELECT COUNT(comments) FROM orders;
````
14. 
````
SELECT COUNT(orderNumber) FROM orders
WHERE comments LIKE '%CAUTION%'; 
````
15. 
````
SELECT AVG(creditLimit) FROM customers;   
````
16.
````
SELECT contactLastName, COUNT(contactLastName) FROM customers
GROUP BY contactLastName
HAVING COUNT(contactLastName)
ORDER BY contactLastName DESC LIMIT 1;
````
17.
````
SELECT status FROM orders
GROUP BY status;  
````
18.
````
SELECT country FROM customers
GROUP BY country; 
````
19.
````
SELECT COUNT(*) FROM orders
WHERE shippedDate IS NULL;
````
20.
````
SELECT COUNT(*) FROM customers
WHERE salesRepEmployeeNumber = (SELECT employeeNumber FROM employees WHERE lastName='PATTERSON' AND firstName='STEVE')
AND creditLimit > 100000;   
````
21.
````
SELECT COUNT(*) FROM orders
WHERE status = 'SHIPPED';
````
22.
````
SELECT ROUND((SELECT COUNT(*) FROM products) / (SELECT COUNT(*) FROM productlines));
````
23.
````
SELECT COUNT(*) FROM products
WHERE quantityInStock < 100;
````
24.
````
SELECT COUNT(*) FROM products
WHERE quantityInStock > 100 AND quantityInStock < 500;
````
25.
````
SELECT COUNT(*) FROM orders
WHERE shippedDate BETWEEN '2004-06-01' AND '2004-09-01';
````
---
### Useful resources 
* https://www.w3schools.com/sql/sql_syntax.asp
* https://www.techrepublic.com/article/sql-basics-select-statement-options/