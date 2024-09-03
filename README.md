CustomerID INT PRIMARY KEY AUTO_INCREMENT:

Data Type: INT
Purpose: Unique identifier for each customer, automatically incremented.
CustomerName VARCHAR(100) NOT NULL:

Data Type: VARCHAR(100)
Purpose: Stores the customer's name with a maximum of 100 characters.
PhoneNumber VARCHAR(15) NOT NULL:

Data Type: VARCHAR(15)
Purpose: Stores the customer's phone number, allowing a maximum of 15 characters.
OrderID INT PRIMARY KEY AUTO_INCREMENT:

Data Type: INT
Purpose: Unique identifier for each order, automatically incremented.
CustomerID INT:

Data Type: INT
Purpose: References the customer who placed the order, linking to CustomerID in the Customers table.
OrderNo VARCHAR(20) UNIQUE NOT NULL:

Data Type: VARCHAR(20)
Purpose: Unique order number, up to 20 characters, with a UNIQUE constraint ensuring no duplicates.
PaymentMode VARCHAR(50) NOT NULL:

Data Type: VARCHAR(50)
Purpose: Stores the payment method used for the order, up to 50 characters.
OrderDate TIMESTAMP DEFAULT CURRENT_TIMESTAMP:

Data Type: TIMESTAMP
Purpose: Stores the date and time the order was placed, automatically set to the current timestamp.
FOREIGN KEY (CustomerID) REFERENCES Customers(CustomerID):

Purpose: Ensures referential integrity by linking CustomerID to the Customers table.
PizzaID INT PRIMARY KEY AUTO_INCREMENT:

Data Type: INT
Purpose: Unique identifier for each pizza type, automatically incremented.
PizzaName VARCHAR(100) NOT NULL:

Data Type: VARCHAR(100)
Purpose: Stores the name of the pizza, up to 100 characters.
PizzaSize ENUM('Small', 'Medium', 'Large') NOT NULL:

Data Type: ENUM
Purpose: Specifies the size of the pizza, limited to Small, Medium, or Large.
Price DECIMAL(10, 2) NOT NULL:

Data Type: DECIMAL(10, 2)
Purpose: Stores the price of the pizza, allowing up to 10 digits in total with 2 decimal places.
SideID INT PRIMARY KEY AUTO_INCREMENT:

Data Type: INT
Purpose: Unique identifier for each side item, automatically incremented.
SideName VARCHAR(100) NOT NULL:

Data Type: VARCHAR(100)
Purpose: Stores the name of the side item, up to 100 characters.
Price DECIMAL(10, 2) NOT NULL:

Data Type: DECIMAL(10, 2)
Purpose: Stores the price of the side item, with 2 decimal places.
DrinkID INT PRIMARY KEY AUTO_INCREMENT:

Data Type: INT
Purpose: Unique identifier for each cold drink, automatically incremented.
DrinkName VARCHAR(100) NOT NULL:

Data Type: VARCHAR(100)
Purpose: Stores the name of the cold drink, up to 100 characters.
Price DECIMAL(10, 2) NOT NULL:

Data Type: DECIMAL(10, 2)
Purpose: Stores the price of the cold drink, with 2 decimal places.
OrderDetailID INT PRIMARY KEY AUTO_INCREMENT:

Data Type: INT
Purpose: Unique identifier for each order detail entry, automatically incremented.
OrderID INT:

Data Type: INT
Purpose: References the Orders table, linking each order detail to a specific order.
PizzaID INT:

Data Type: INT
Purpose: References the PizzaTypes table, linking to a specific pizza.
SideID INT:

Data Type: INT
Purpose: References the Sides table, linking to a specific side item (can be NULL if no side is ordered).
DrinkID INT:

Data Type: INT
Purpose: References the ColdDrinks table, linking to a specific drink (can be NULL if no drink is ordered).
Quantity INT NOT NULL:

Data Type: INT
Purpose: Specifies the quantity of the item ordered.
Foreign Keys:

Each FOREIGN KEY constraint ensures referential integrity by linking to the respective primary key in the related tables (Orders, PizzaTypes, Sides, ColdDrinks).

Data Type: VARCHAR
Names and phone numbers are stored in the Customers table with VARCHAR data type, as explained earlier.

Data Type: VARCHAR, ENUM, DECIMAL
Pizza names, sizes (ENUM), and prices (DECIMAL) are stored in the PizzaTypes table.
Insert Data into Sides Table

Side names and prices are stored in









