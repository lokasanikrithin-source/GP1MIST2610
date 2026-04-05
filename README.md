
# MIST 4610 Group Project 1

## Group Members:

1. Donovan D'Silva - [repo](https://github.com/donmelsil/MIST4610_Group-Project)
2. Noah Hammond	- [repo](https://github.com/NoahHammond1/MIST4610_CoffeeShop_Project/tree/main)
3. Chase Lin - [repo](https://github.com/cinnamotz/mist4610gp1/tree/main)
4. Krithin Lokasani	- [repo](https://github.com/lokasanikrithin-source/GP1MIST2610)
5. Jessica Ngo - [repo](https://github.com/jn83499/Mist4610_Group-Project)

## Problem Description
We were assigned a task to model and build a relational database for the general operations of a coffee shop. The central entity in the model is the Orders entity, as it represents each transaction made by customers and serves as the core around which the rest of the system operates. Orders connect key components of the business, including customers, employees, products, and payments.

The coffee shop operates with related entities such as products (menu items), suppliers, and loyalty accounts, all supporting daily operations. Suppliers provide the necessary ingredients and inventory, while customer and order data allow the business to track consumer behavior and service interactions.

We are interested in accurately modeling these relationships, generating sample data, and populating the entities and their attributes. We aim to perform functional queries on this data to provide important and valuable business insights, such as identifying popular menu items, managing inventory needs, and supporting decision-making for purchasing and operational efficiency.
## Data Model

![Date Model Screenshot](https://github.com/user-attachments/assets/d49fc096-50be-42ee-8ef5-bb0dfb922feb)
## Data Dictionary
![Employee Data Dictionary](https://github.com/user-attachments/assets/16eb99a6-1eff-4cb7-a8e4-52683a99ef8e)
![Customer Data Dictionary](https://github.com/user-attachments/assets/443cfa8b-8651-4a4f-968a-b8a4500a6143)
![Category and Store Location Data Dictionary](https://github.com/user-attachments/assets/3a8921d9-2bc0-45e8-b8b2-dfce43adf7c8)
![Orders Data Dictionary](https://github.com/user-attachments/assets/109f23db-613f-4448-9357-a0fb38a7c6df)
![OrderItems and Dictionary](https://github.com/user-attachments/assets/30a12863-8cef-4071-86c7-f84ab8bca830)
![Products Data Dictionary](https://github.com/user-attachments/assets/e0bdccb7-78af-41ff-86d4-a99b3180dd9d)
![Loyalty Account and Payment Data Dictionary](https://github.com/user-attachments/assets/0d7069a5-e563-45d1-a3c0-a6ffa9e4ddda)
![Supplier and Product Supplier Data Dictionary](https://github.com/user-attachments/assets/84054961-e362-4b31-9982-4095a0f2860f)
## Queries
| Feature                     | Q1 | Q2 | Q3 | Q4 | Q5 | Q6 | Q7 | Q8 | Q9 | Q10 |
|----------------------------|----|----|----|----|----|----|----|----|----|-----|
| Multiple Table Join        | X  | X  |    | X  | X  |    | X  |    |    |     |
| Subquery                   | X  |    |    | X  |    |    |    |    |  X |     |
| GROUP BY                   | X  | X  |    |    | X  | X  |    |    |    |     |
| GROUP BY with HAVING       | X  |    |    |    |    |    |    |    |    |     |
| Multi-condition WHERE      |    |    |    |  X |    |    |    |    |  X |     |
| Built-in Functions         | X  | X  | X  |    |    | X  |    |    |    |     |
| REGEXP                     |    |    | X  |    |    |    |    | X  |    |     |
| NOT EXISTS                 |    |    |    |    |    |    |    |    |  X |     |
1. Query 1 finds customers who spend more than average by comparing each customer’s total spending to the overall average payment.
   
![Query1](https://github.com/user-attachments/assets/b6cbaa6c-c86a-4513-a792-28521b4888a6)

Query 1 allows managers to identify the customers who spend the most, helping them focus on high-value customers. This allows them to create targeted promotions, loyalty rewards, and  strategies to increase revenue. It also helps them make smarter business decisions by understanding customer spending patterns.

2. Query 2 adds up the quantity sold for each product and groups the results by product name so you can see the total units sold for each individual product.
   
![Query2](https://github.com/user-attachments/assets/0706f9e3-bc22-4e4e-8539-568eec30060d)

Query 2 allows managers to see which items are popular so they know what is selling well and what might not be selling well. By identifying top-performing items, managers can know which products to restock or promote more of. It also helps with inventory planning and forecasting demand, so they don’t overstock slow items or run out of popular ones.

3. Query 3 finds the total amount of orders from Decemember 2025.

![Query3](https://github.com/user-attachments/assets/e3fe78ac-222a-4642-b5a6-0b30bd5ba2f1)
Query 3 allows for managers and employees to see the total amount of orders for a certain month. In the case of query 3 it is for the month of December. This is useful for managers as they can compare the total amount of orders in December to those of other months, which would help to show how orders increase or decrease from month to month. It would help to show how busy a store is based on the total monthly orders.

4. Query 4 lists the total revenue generated by credit card payments during 2026. The results are ordered in descending order of total revenue.

![Query4](https://github.com/user-attachments/assets/656f2766-f56d-44eb-af61-960298c94199)
Query 4 helps managers identify which customers are making large purchases using only credit cards during the 2026 fiscal year. If they notice that most of these high-value transactions come from a small group of repeat customers, it suggests those customers are especially engaged and valuable to the business. With that insight, managers could consider introducing a premium rewards program or offering exclusive perks to these high-spending customers, encouraging them to stay loyal and potentially increasing overall transaction values across store locations.

5. Query 5 lists each store location alongside its total number of orders, total revenue generated, and average order value. The results are ordered in descending order of total revenue.

![Query5](https://github.com/user-attachments/assets/0aa6216a-1801-434c-b7a9-57cd7c9501d9)
Query 5 allows managers to compare the performances of each store location against each other in a multitude of ways. The ways are total orders, total revenue, and average order value. Total orders would allow managers to understand how many total orders are being processed by each store relative to their counterparts, to understand which locations are seeing more volume. Total revenue gives a little more of this understanding, by allowing managers to dissect even further into which stores are the most profitable. Average order value allows managers to better understand which stores are able to generate more value based on each individual order, possibly justifying raised prices or expanded premium offerings at certain locations.

6. Query 6 finds what payment method is used the most amongst all the stores.

![Query6](https://github.com/user-attachments/assets/77b83ac0-a04a-4cb6-a621-3f6a6592ba4c)
Query 6 allows for managers to see what type of payment method is the most popular. The query shows that cash is used the least out of all payment methods. Managers might be able to adopt a card and mobile payments only store policy, since they would be faster for store purchases. It would take more time having to count cash and give that back to the customer if they decide to use that as a method of payment.

7. Query 7 shows the amount of loyalty points attached to a customer ID in descending order.

![Query7](https://github.com/user-attachments/assets/7033e2a7-e0d6-43b9-9d2c-bc0f95b471c9)
Query 7 allows for customers to see the total amount of loyalty points they have. This is useful for when they need to redeem for different rewards. It would also be useful for employees and managers to see them when during or after a purchase to help loyalty point redemption.


8. Query 8 shows all orders placed after March 1, 2026 with order numbers that start with 3.

![Query8](https://github.com/user-attachments/assets/a96df327-3304-4316-a245-0d4a53d4609a)
Query 8 allows businesses to see recent transactions and analyze them while focusing on specific categories of orders identified the starting number of their order number. For instance, the number 3 could only relate to in-store transactions so businesses would look at these orders if they want to inquire about them in any way. This is useful for managers and employees when evaluating short-term performance and understanding consumer behavior. 


9. Query 9 shows customers that have not yet been served by specific employees at a given store location.

(![Query9](https://github.com/user-attachments/assets/27b963e1-c1c9-43f6-9e12-bc93587f2c2a))


Query 9 allows managers to understand business distribution among employees, identify oppurtunities for employees to engage with new customers, and improve overall customer experience by ensuring a more balanced interaction with customers and employees. 

10. Query 10 shows the suppliers who supply more than 1 product that are priced over 2 dollars.

![Query10](https://github.com/user-attachments/assets/c9ebd27a-d7bf-4515-91d2-89060bb1f0f2)
Query 10 allows managers to see which suppliers provide the most products to the coffeeshop, focusing on products that are currently available and priced over $2.00. Managers can use this information to make better decisions about supplier relationships and inventory planning. Suppliers with more products and higher value products may be prioritized for future supply orders, and the suppliers with fewer products can be reconsidered for either improving relationships or terminating them.




## Database information
Name of Database: al_Group_21482_G7

Additional Info: Each query listed above is marked in the database used stored procedures which are called through the following format: CALL DNCKJ_Q() where "()" is the query number.
