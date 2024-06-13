# Jpin

# monitoring system

This is an example of a class diagram using Mermaid in GitHub.

```mermaid
classDiagram
    class Main {
        +main(String[] args)
    }

    class Order {
        -int quantity
        -Delivery delivery
        -String paymentMethod
        +Order(int quantity, Delivery delivery, String paymentMethod)
    }

    class Delivery {
        -String address
        -String phoneNumber
        -LocalDateTime deliveryDateTime
        +Delivery(String address, String phoneNumber, LocalDateTime deliveryDateTime)
    }

    Main --> Order
    Order --> Delivery

