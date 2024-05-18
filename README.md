# Jpin
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


