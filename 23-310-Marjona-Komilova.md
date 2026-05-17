# Online Food Delivery System

## Stage 1. Requirements

### Functional Requirements

1. Users can register and log into the system.
2. Customers can browse restaurants and food menus.
3. Users can place food orders online.
4. The system sends order status notifications to users.
5. Admins can manage restaurants, menus, and orders.

### Non-Functional Requirements

1. The system should support at least 1000 active users simultaneously.
2. Page loading time should not exceed 3 seconds.
3. User data must be protected with secure authentication.
4. The system should be available 99.9% of the time.
5. The application should work on both mobile and desktop devices.

---

# Stage 2. Architecture

## Option 1 — Monolithic Architecture

### System Diagram

```text
[ Client App ]
       |
       v
[ Monolithic Server ]
       |
       v
[ Database ]


Advantages
Easy to develop for small projects
Faster initial development
Simple deployment process
Easier debugging
Disadvantages
Difficult to scale large systems
One error can affect the whole application
Harder to maintain as the project grows


Option 2 — Microservices Architecture
System Diagram

[ Client App ]
       |
       v
[ API Gateway ]
   |      |      |
   v      v      v
[ User ] [ Order ] [ Payment ]
 Service   Service   Service
       \      |      /
        \     |     /
         v    v    v
          [ Database ]


Advantages
Easier to scale services independently
Better fault isolation
Easier maintenance for large systems
Teams can work independently
Disadvantages
More complex development
Harder deployment and monitoring
Requires more server resources
Best Architecture Choice

For this project, the Monolithic Architecture is better because the system is relatively small and easier to manage with a single server application. It allows faster development and simpler deployment. Microservices architecture is more suitable for very large systems with many users and services.
