#Bamazon

Week of 12 HW: Node.js & MySQL FOR UCLA EXTENSION CODING BOOTCAMP

### Overview

In this activity, you'll be creating an Amazon-like storefront with the MySQL skills you learned this week. The app will take in orders from customers and deplete stock from the store's inventory. As a bonus task, you can program your app to track product sales across your store's departments and then provide a summary of the highest-grossing departments in the store. 


#My Videos
[click here to see My Video Demonstration](https://youtu.be/UnZctQ2lnEU) 

#### Instructions:

### Challenge #1: Customer View (Minimum Requirement)

1. Create a MySQL Database called `Bamazon`.

2. Then create a Table inside of that database called `Products`.

3. The products table should have each of the following columns:

	* ItemID (unique id for each product)

	* ProductName (Name of product)

	* DepartmentName 

	* Price (cost to customer)

	* StockQuantity (how much of the product is available in stores)

4. Populate this database with around 10 different products. (i.e. Insert "mock" data rows into this database and table).

5. Then create a Node application called `BamazonCustomer.js`. Running this application will first display all of the items available for sale. Include the ids, names, and prices of products for sale.

6. The app should then prompt users with two messages. 
	* The first should ask them the ID of the product they would like to buy. 
	* The second message should ask how many units of the product they would like to buy.

7. Once the customer has placed the order, your application should check if your store has enough of the product to meet the customer's request. 
	* If not, the app should log a phrase like `Insufficient quantity!`, and then prevent the order from going through.

8. However, if your store *does* have enough of the product, you should fulfill the customer's order. 
	* This means updating the SQL database to reflect the remaining quantity.
	* Once the update goes through, show the customer the total cost of their purchase.

---------------------------------

* If this activity took you between 8-10 hours, then you've put enough time into this assignment. Feel free to stop here -- unless you want to take on the next challenge.

------------------------------------

### Challenge #2: Manager View (Next Level)

* Create a new Node application called `BamazonManager.js`. Running this application will:

	* List a set of menu options: 
		* View Products for Sale 
		* View Low Inventory
		* Add to Inventory
		* Add New Product

	* If a manager selects `View Products for Sale`, the app should list every available item: the item IDs, names, prices, and quantities.

	* If a manager selects `View Low Inventory`, then it should list all items with a inventory count lower than five.

	* If a manager selects `Add to Inventory`, your app should display a prompt that will let the manager "add more" of any item currently in the store. 

	* If a manager selects `Add New Product`, it should allow the manager to add a completely new product to the store.

---------------------------------

* If you finished Challenge #2 and put in all the hours you were willing to spend on this activity, then rest easy! Otherwise continue to the next and final challenge.

------------------------------------

### Challenge #3: Executive View (Final Level)

1. Create a new MySQL table called `Departments`. Your table should include the following columns:

	* DepartmentID

	* DepartmentName

	* OverHeadCosts (A dummy number you set for each department)

	* TotalSales

2. Modify your `BamazonCustomer.js` app so that when a customer purchases anything from the store, the program will calculate the total sales from each transaction.
	* Add the revenue from each transaction to the `TotalSales` column for the related department.
	* Make sure your app still updates the inventory listed in the `Products` column.

3. Create another Node app called `BamazonExecutive.js`. Running this application will list a set of menu options: 
	* View Product Sales by Department 
	* Create New Department

4. When an executive selects `View Product Sales by Department`, the app should display a summarized table in their terminal/bash window. Use the table below as a guide. 

	| DepartmentID | DepartmentName | OverHeadCosts | ProductSales | TotalProfit |
	|--------------|----------------|---------------|--------------|-------------|
	| 01           | Electronics    | 10000         | 20000        | 10000       |
	| 02           | Clothing       | 60000         | 100000       | 40000       |


5. The `TotalProfit` should be calculated on the fly using the difference between `OverheadCosts` and `ProductSales`. `TotalProfit` should not be stored in any database. You should use a custom alias. 

6. If you can't get the table to display properly after a few hours, then feel free to go back and just add `TotalProfit` to the `Departments` table.

	* Hint: You will need to use joins to make this work. 

	* Hint: You may need to look into grouping in MySQL.

	* **HINT**: There may be an NPM package that can log the table to the console. What's is it? Good question :)

-------
### One More Thing
If you have any questions about this project or about the material we covered, the instructor and your TAs are only a Slack message away.

**Good Luck!**

## Copyright
Coding Boot Camp (C) 2016. All Rights Reserved.