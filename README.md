# Eureka Service Discovery

Eureka Service Discovery is a project developed with Spring Boot and Eureka, designed to display a panel for managing microservices

## :clipboard: Requirements

> **Note:**  
> To run this project, you need:
>
>- **Java 17** or a higher version.
>- **Spring Boot** (version 3.4.4).

## :gear: Port Configuration

1. In the `application.properties` file, you can set the port in which you want to run your discovery service. If you do not configure a port, the microservice will automatically run on port 8761.

    ```properties
    server.port=8761
    ```

## :gear: Customer Service Configuration

1.  **Customer Service** is a project that creates a microservice for customer management which will be attached to our Eureka panel. You need to download the CUstomer Service **[here](https://github.com/AndresMaldonado200338/Customer-Service)**.
2. Follow the steps to run **Customer Service**, ensuring the port in `eureka.client.service-url.defaultZone` must be the same as the `server.port` in your `application.properties` file in this project.

    In this project:
    ```properties
    server.port=8761
    ```

    In **Customer Service**:
    ```properties
    eureka.client.service-url.defaultZone=http://localhost:8761/eureka
    ```

## :heavy_check_mark: Running the Project

1. Download the **Customer Service** and this project, ensuring they are located in appropriate places.
2. Open both projects in your preferred IDE.
3. Run first the main file of **Eureka** `EurekaApplication.java` located at `src/main/java/edu/uptc/swii/eureka`.
4. Then run the main file of **Customer Service** `CustomerserviceApplication.java` located at `src/main/java/edu/uptc/swii/customerservice`.

**Eureka Service Discovery** will run at the URL `http://localhost:PORT`, where `PORT` is the value you configured earlier in the `application.properties` file.

**Customer Service** will be found in the Eureka dashboard under the **“Instances currently registered with Eureka”** section or by accessing it directly at `http://localhost:PORT`, where `PORT` is the value configured in the `application.properties` file.

## :handshake: Contributors

This project was created by:

### - Juan David Ochoa
[![Github](https://img.shields.io/badge/github-%2324292e.svg?&style=for-the-badge&logo=github&logoColor=white)](https://github.com/JuanDavid0)  
[![LinkedIn](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/juan-david-ochoa-pinilla/)

### - William Cely
[![Github](https://img.shields.io/badge/github-%2324292e.svg?&style=for-the-badge&logo=github&logoColor=white)](https://github.com/WilliamC111)  
[![LinkedIn](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/williamcelyl%C3%B3pez/)

### - Andrés Maldonado
[![Github](https://img.shields.io/badge/github-%2324292e.svg?&style=for-the-badge&logo=github&logoColor=white)](https://github.com/AndresMaldonado200338)  
[![LinkedIn](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/amaldonados/)
