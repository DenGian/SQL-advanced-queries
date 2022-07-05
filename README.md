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
   
````
13.
````

````
14. 
````
 
````
15. 
````
   
````
---
### Useful resources 
* https://www.w3schools.com/sql/sql_syntax.asp