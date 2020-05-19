# Shopping Cart - Microservice Sample

Shopping cart web application is online shopping portal. It is developed using microservices architecture.

## Features
Microservices is an architecture wherein all the components of the system are put into individual components, which can be built, deployed, and scaled individually.

In Shopping cart there are 3 services- Eureka-Server, Product-Catalog, WebServer.
Eureka Server
Microservices use service discovery which acts as a guide to find the route of communication between each of them. Netflix Eureka service registry is used to build a client that both registers itself with the registry and uses it to resolve its own host. First we need a Eureka Service registry. We can use Spring Cloud’s @EnableEurekaServer to stand up a registry with which other applications can communicate. This is a regular Spring Boot application with one annotation (@EnableEurekaServer) added to enable the service registry. 

Product-Catalog
Services in a microservice architecture (MSA) are often processes that communicate over a network to fulfill a goal using technology-agnostic protocols such as HTTP. Services in a microservice architecture are independently deployable. Services are organized around business capabilities.Product-Catalog service is used to fetch data from products table in MS SQL database. Fetched data can be view using http:\\localhost\8088\Catalog

WebServer
Webserver is another service which renders the views. There are two views; home.html and cart.html. Home.html displays the product catalog. Selected items are added to cart. The products details for product catalog is obtained from product catalog service.

## Deployment 
In browser https://localhost/8087/home
This will display the Home page of the shopping site.
