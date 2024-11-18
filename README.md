# Spring-REST-Data-TP---Bank

This project demonstrates a **Spring Boot REST Data** application for managing bank accounts. It showcases a simple architecture with entities, repositories, configuration, and Swagger integration for API documentation.

## Project Structure

```
.
├── main
│   ├── java
│   │   └── org
│   │       └── marouanedbibih
│   │           └── bankrestdata
│   │               ├── BankRestDataApplication.java
│   │               ├── compte
│   │               │   ├── Compte.java
│   │               │   ├── CompteRepository.java
│   │               │   └── TypeCompte.java
│   │               └── config
│   │                   ├── DatabaseInitializer.java
│   │                   └── SwaggerConfig.java
│   └── resources
│       └── application.properties
└── test
    └── java
        └── org
            └── marouanedbibih
                └── bankrestdata
                    └── BankRestDataApplicationTests.java
```

## Features

- **Entity Management:** The `Compte` entity represents bank accounts with associated types using `TypeCompte`.
- **Repository Layer:** `CompteRepository` for database operations.
- **Database Initialization:** `DatabaseInitializer` preloads data into the database.
- **Swagger API Documentation:** `SwaggerConfig` enables interactive API documentation.
- **Unit Testing:** Tests are written in `BankRestDataApplicationTests`.

## Setup and Run

### Prerequisites

- Java 21
- Maven
- H2 Database
- Swagger UI
- Spring Data REST
- Spring Data JPA

### Steps

1. Clone the repository:
   ```bash
   git clone https://github.com/marouanedbibih/Spring-REST-Data-TP---Bank
   cd spring-rest-data-tp---bank
   ```

2. Build the project:
   ```bash
   mvn clean install
   ```

3. Run the application:
   ```bash
   mvn spring-boot:run
   ```

4. Access Swagger documentation at:
   ```
   http://localhost:8080/swagger-ui.html
   ```

### Configuration

Update database settings in `src/main/resources/application.properties` as needed.

## Endpoints

| HTTP Method | Endpoint         | Description            |
|-------------|------------------|------------------------|
| GET         | `/comptes`       | List all bank accounts |
| POST        | `/comptes`       | Create a new account   |
| PUT         | `/comptes/{id}`  | Update an account      |
| DELETE      | `/comptes/{id}`  | Delete an account      |

## Project Modules

### Entity: `Compte`

Represents a bank account with attributes like account type and balance.

### Repository: `CompteRepository`

Provides CRUD operations for the `Compte` entity.

### Configurations

- **DatabaseInitializer:** Initializes the database with sample data.
- **SwaggerConfig:** Configures Swagger UI for API documentation.

## Testing

Run unit tests with:
```bash
mvn test
```