# SQL
SQL Portfolio
-- Create a cafe menu database 

CREATE TABLE cafe (id INTEGER PRIMARY KEY, category TEXT, name TEXT, calories INTEGER, price INTEGER, customer_rating INTEGER); 

INSERT INTO cafe VALUES (1, "coffee", "Americano", 15, 3.99, 5);
INSERT INTO cafe VALUES (2, "coffee", "Dark Roast Coffee", 5, 3.99, 4.7);
INSERT INTO cafe VALUES (3, "coffee", "Decaf Roast", 15, 3.99, 4.5);
INSERT INTO cafe VALUES (4, "coffee", "Espresso", 10, 2.99, 5);
INSERT INTO cafe VALUES (5, "coffee", "Cappuccino", 130, 3.99, 4.9); 
INSERT INTO cafe VALUES (6, "tea", "Iced Black Tea", 10, 3.99, 4.5);
INSERT INTO cafe VALUES (7, "tea", "Hot Tea", 15, 3.99, 4);  
INSERT INTO cafe VALUES (8, "coffee", "Cafe Latte", 180, 4.99, 4.8);
INSERT INTO cafe VALUES (9, "coffee", "Vanilla Latte", 240, 5.50, 5);
INSERT INTO cafe VALUES (10, "coffee", "Sweet Potato Latte", 380, 5.50, 4.4);
INSERT INTO cafe VALUES (11, "coffee", "Snickers Peanut Butter Latte", 410, 6.50, 5);
INSERT INTO cafe VALUES (12, "coffee", "Hazelnut Latte", 390, 5.50, 4.9);
INSERT INTO cafe VALUES (13, "coffee", "Caramel Latte", 410, 5.50, 5);
INSERT INTO cafe VALUES (14, "sweets", "Matcha Cake", 320, 4.50, 4.7);
INSERT INTO cafe VALUES (15, "sweets", "Strawberry Shortcake", 325, 4.50, 4.9);
INSERT INTO cafe VALUES (16, "sweets", "Tres Leches Cake", 390, 4.5, 5);
INSERT INTO cafe VALUES (17, "sweets", "Choco Flan", 410, 4.50, 4.9);

-- display only the coffee items under 200 calories && list them from the least to most pricey 
SELECT *
FROM cafe
WHERE category = "coffee" AND calories <= 200 
ORDER BY price asc

-- what is average price of items in the sweets category?
SELECT AVG(price)
FROM cafe
WHERE category = 'sweets' 

-- what are the five most popular items on the menu?
SELECT name, price, customer_rating
FROM cafe
ORDER BY customer_rating desc
LIMIT 5
