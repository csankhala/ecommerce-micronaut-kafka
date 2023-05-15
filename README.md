# ecommerce-micronaut-kafka
This is learning project created to develop microservices architecture with Micronaut and Kafka

## Requirements (Generated by ChatGPT!)
Example: An e-commerce application that uses Kafka to process orders.

The application consists of several microservices: a **product catalog service**, a **shopping cart service**, an **order service**, and a **payment service**.

When a user adds a product to their shopping cart, the shopping cart service sends a message to a Kafka topic called "cart-updated".

The order service subscribes to the "cart-updated" topic, and processes incoming messages to create an order. The order service uses the product catalog service to get product information, and the payment service to process payments.

When an order is created, the order service sends a message to a Kafka topic called "order-created".

The shipping service subscribes to the "order-created" topic, and processes incoming messages to initiate the shipping process.

As the **shipping process** progresses, the shipping service sends status updates to a Kafka topic called "shipping-updates".

The **customer service** subscribes to the "shipping-updates" topic, and sends order status updates to the customer.

# Services (Repos)
1. [Product Catalog Service](https://github.com/csankhala/ProductCatalogService)
2. [Shopping Cart Service](https://github.com/csankhala/ShoppingCartService)
3. [Order Service](https://github.com/csankhala/OrderService)
4. [Payment Service](https://github.com/csankhala/PaymentService)
5. [Customer Service](https://github.com/csankhala/CustomerService)
6. [Shipping Service](https://github.com/csankhala/ShippingService) 

# Good First Issue List from this project

[Good First Issue list](good-first-issue-list.md)
