# Schemas-for-a-shopping-app
Design the NoSQL schemas for a shopping app. #SpecialManInternship2023

## Question
Design the NoSQL schemas for a shopping app.

**User story**: As a shopper, I want to be able to browse a catalog of products and add items to my shopping cart. I also want to be able to view the contents of my cart and adjust the quantity of items in my cart. Finally, I want to be able to place an order and receive confirmation of my order.


## Solution

### Requirements:
- A catalog of products that can be browsed by shoppers
- The ability for shoppers to add items to their cart and adjust quantities
- The ability for shoppers to view the contents of their cart and adjust quantities
- The ability for shoppers to place an order and receive confirmation.


### Entities Needed
- Products
- Customers
- Orders
- Cart


### Relationship
- Each customer can have one or many orders
- Each order can have one or many products
- Each customer can have one cart
- Each cart can have one or many products


![Busola and Genius](https://user-images.githubusercontent.com/55829039/222960849-9fd10376-b89c-4c6b-8f96-6c9213954c39.png)



### Features of the Shopping App:
-  Browse catalog: The user should be able to browse a catalog of products with images and descriptions.
-  Add items to shopping cart: The user should be able to add items to their shopping cart by clicking on an "Add to Cart" button on the product detail page.
-  View shopping cart contents: The user should be able to view the contents of their shopping cart, including the name, image, and price of each item, as well as the total cost of their order so far.
- Adjust quantity of items in cart: The user should be able to adjust the quantity of each item in their cart or remove items altogether.
- Place an order: The user should be able to place an order by entering their shipping and billing information, and selecting a payment method.
- Receive confirmation: The user should receive a confirmation message or email that their order has been received and processed successfully.

In this schema, the `Customer` collection stores information about the customers, including their `name`, `email`, and `address`. Each customer has a cart and can have one or many orders. The `Cart` collection stores the items that a customer has added to their `cart`, including the product ID and quantity. The `Product` collection stores information about the products, including the `name`, `description`, `price`, and `image URL`. The `Order` collection stores information about the orders, including the customer ID, items, total price, status, and creation date.


## API End points
### Products
**`GET /api/products`**: Get a list of all products

**`GET /api/products/:id`**: Get a specific product by ID

**`POST /api/products`**: Create a new product

**`PUT /api/products/:id`**: Update a specific product by ID

**`DELETE /api/products/:id`**: Delete a specific product by ID

### Customers

**`GET /api/customers`**: Get a list of all customers

**`GET /api/customers/:id`**: Get a specific customer by ID

**`POST /api/customers`**: Create a new customer

**`PUT /api/customers/:id`**: Update a specific customer by ID

**`DELETE /api/customers/:id`**: Delete a specific customer by ID

### Carts

**`GET /api/carts/:id`**: Get the cart for a specific customer by customer ID

**`POST /api/carts/:id/items`**: Add an item to the cart for a specific customer by customer ID

**`PUT /api/carts/:id/items/:itemId`**: Update the quantity of an item in the cart for a specific customer by customer ID and item ID

**`DELETE /api/carts/:id/items/:itemId`**: Remove an item from the cart for a specific customer by customer ID and item ID


### Orders
**`GET /api/orders`**: Get a list of all orders

**`GET /api/orders/:id`**: Get a specific order by ID

**`POST /api/orders`**: Create a new order

**`PUT /api/orders/:id`**: Update a specific order by ID

**`DELETE /api/orders/:id`**: Delete a specific order by ID
