-- Create a grocery store database 

CREATE TABLE Store (id INTEGER PRIMARY KEY, ITEM TEXT, Section Text, Price Integer, quantity Integer);

INSERT INTO store VALUES (1, "chips", "snacks", 3.50, 65);
INSERT INTO store VALUES (2, "water", "drinks", 2.50, 75);
INSERT INTO store VALUES (3, "crackers", "snacks", 2.00, 40);
INSERT INTO store VALUES (4, "pizza", "frozen", 4.99, 70);
INSERT INTO store VALUES (5, "apple", "produce", 1.00, 21);
INSERT INTO store VALUES (6, "pancake mix", "breakfast", 2.99, 35);
INSERT INTO store VALUES (7, "Pepsi", "drinks", 4.99, 45);
INSERT INTO store VALUES (8, "diapers", "baby", 11.99, 40);
INSERT INTO store VALUES (9, "broccoli", "frozen", 2.99, 50);
INSERT INTO store VALUES (10, "cereal", "breakfast", 2.99, 45);
INSERT INTO store VALUES (11, "formula", "baby", 10.99, 58);
INSERT INTO store VALUES (12, "cookies", "snacks", 1.99, 80);
INSERT INTO store VALUES (13, "hamburger", "meat", 5.99,30);
INSERT INTO store VALUES (14, "juice", "drinks", 1.99, 50);
INSERT INTO store VALUES (15, "chicken", "meat", 7.99, 38);


--display the database ordered by price. 
SELECT * FROM store
ORDER BY price desc; 

--what is the avg price of items in the drinks section? 
SELECT AVG(price) "avg drinks item price"
FROM store
where section='drinks'; 

--what are the most 5 popular items? 
SELECT item, price, quantity
FROM store
order by quantity desc
limit 5; 

-- what is the most expensive price for snacks

Select MAX (price) from store 
where section= 'snacks'; 

--what is the most expensive item

Select item,price
From store
order by price desc
limit 1;






