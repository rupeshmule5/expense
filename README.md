# Expense Service

## Overview
The Expense Service provides APIs to manage expenses. Users can create, retrieve, and delete expense entries.

## Requirements
- Java 17+
- Maven 3+
- H2 Database

## Running the Service

1. Clone the repository:
   cd expense-service

2. Build the application:
   mvn clean install

3. Run the application:
   mvn spring-boot:run

4. Access the H2 Console:
   - URL: [http://localhost:8081/h2-console](http://localhost:8081/h2-console)
   - JDBC URL: `jdbc:h2:mem:expensedb`
   - Username: `sa`
   - Password: `password`

5. Access Swagger UI:
   - URL: [http://localhost:8081/swagger-ui.html](http://localhost:8081/swagger-ui.html)

## API Endpoints

### Create Expense
- **URL**: `/api/v1/expenses`
- **Method**: POST
- **Body**:
  json
  {
    "description": "Lunch at cafe",
    "amount": 15.0,
    "category": "Food"
  }
 

### Get All Expenses
- **URL**: `/api/v1/expenses`
- **Method**: GET

### Get Expense by ID
- **URL**: `/api/v1/expenses/{id}`
- **Method**: GET

### Delete Expense
- **URL**: `/api/v1/expenses/{id}`
- **Method**: DELETE
