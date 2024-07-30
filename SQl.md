# SQL Queries for Preowned Cars Dataset

This document contains SQL queries used to analyze the preowned cars dataset.

## 1. Select All Data from `preowned_cars` Table

SELECT * FROM preowned_cars;

## 2. Total Number of Cars

This query counts the total number of cars in the dataset.

SELECT COUNT(*) AS total_cars
FROM preowned_cars;

## 3. Most Preferred Variants

This query finds the most preferred car variants, limited to the top 10.


SELECT name, COUNT(*) AS frequency
FROM preowned_cars
GROUP BY name
ORDER BY frequency DESC
LIMIT 10;


## 4. Type of Fuel

This query shows the types of fuel used in the cars, limited to the top 3 most frequent fuel types.


SELECT fuel, COUNT(*) AS frequency
FROM preowned_cars
GROUP BY fuel
ORDER BY frequency DESC
LIMIT 3;

## 5. Average Type of Transmission Preferred by Customers
This query finds the average type of transmission preferred by customers.

SELECT transmission, COUNT(*) AS frequency
FROM preowned_cars
GROUP BY transmission
ORDER BY frequency ASC
LIMIT 5;


## 6. Average Kilometers Driven
This query calculates the average kilometers driven for the cars in the dataset.

SELECT AVG(km_driven) AS average_km_driven
FROM preowned_cars;


## 7. Year of Manufacture

This query shows the distribution of cars based on their year of manufacture.

 SELECT year, COUNT(*) AS frequency
 FROM preowned_cars
 GROUP BY year
 ORDER BY frequency DESC;


## 8. Number of Owners

This query provides the distribution of cars based on the number of previous owners.

SELECT owner, COUNT(*) AS frequency
FROM preowned_cars
GROUP BY owner
ORDER BY frequency DESC;


## 9. Selling Price of the Cars

This query gives insights into the selling prices of different cars.

SELECT selling_price, COUNT(*) AS frequency
FROM preowned_cars
GROUP BY selling_price
ORDER BY frequency DESC;

## 10. Type of Seller

This query categorizes the cars based on the type of seller (dealer or individual).

SELECT seller_type, COUNT(*) AS frequency
FROM preowned_cars
GROUP BY seller_type;




