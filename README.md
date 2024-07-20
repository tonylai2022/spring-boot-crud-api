# Spring Boot CRUD API Example

This is a simple Spring Boot application that provides a RESTful API for managing items. The application supports basic CRUD (Create, Read, Update, Delete) operations.

## Table of Contents

- [Features](#features)
- [Technologies](#technologies)
- [Setup](#setup)
- [Running the Application](#running-the-application)
- [API Endpoints](#api-endpoints)
- [Testing with Postman](#testing-with-postman)

## Features

- Create a new item
- Retrieve all items
- Retrieve a specific item by ID
- Update an existing item
- Delete an item

## Technologies

- Java 17
- Spring Boot 3.3.2
- Spring Data JPA
- H2 Database (in-memory)
- Maven

## Setup

1. **Clone the repository**:

    ```bash
    git clone https://github.com/yourusername/spring-boot-crud-api.git
    cd spring-boot-crud-api
    ```

2. **Ensure you have JDK 17 installed**:

    ```bash
    java -version
    ```

    If not, download and install JDK 17 from the [official Oracle website](https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html).

3. **Ensure you have Maven installed**:

    ```bash
    mvn -version
    ```

    If not, download and install Maven from the [official Apache Maven website](https://maven.apache.org/download.cgi).

## Running the Application

1. **Navigate to the project directory**:

    ```bash
    cd path/to/your/project
    ```

2. **Build the project**:

    ```bash
    mvn clean install
    ```

3. **Run the application**:

    ```bash
    mvn spring-boot:run
    ```

4. The application should start on `http://localhost:8080`.

## API Endpoints

### Create a new item

- **URL**: `/api/items`
- **Method**: `POST`
- **Headers**: `Content-Type: application/json`
- **Body**:

    ```json
    {
        "name": "Sample Item",
        "value": 100
    }
    ```

- **Response**: `201 Created`

### Retrieve all items

- **URL**: `/api/items`
- **Method**: `GET`
- **Response**: `200 OK`

### Retrieve a specific item by ID

- **URL**: `/api/items/{id}`
- **Method**: `GET`
- **Response**: `200 OK` if the item is found, `404 Not Found` if the item is not found

### Update an existing item

- **URL**: `/api/items/{id}`
- **Method**: `PUT`
- **Headers**: `Content-Type: application/json`
- **Body**:

    ```json
    {
        "name": "Updated Item",
        "value": 150
    }
    ```

- **Response**: `200 OK` if the item is updated, `404 Not Found` if the item is not found

### Delete an item

- **URL**: `/api/items/{id}`
- **Method**: `DELETE`
- **Response**: `200 OK` if the item is deleted, `404 Not Found` if the item is not found

## Testing with Postman

1. **Create a new POST request** to create an item:

    - URL: `http://localhost:8080/api/items`
    - Method: `POST`
    - Headers: `Content-Type: application/json`
    - Body:

        ```json
        {
            "name": "Sample Item",
            "value": 100
        }
        ```

2. **Create a new GET request** to retrieve all items:

    - URL: `http://localhost:8080/api/items`
    - Method: `GET`

3. **Create a new GET request** to retrieve a specific item by ID:

    - URL: `http://localhost:8080/api/items/{id}`
    - Method: `GET`

4. **Create a new PUT request** to update an existing item:

    - URL: `http://localhost:8080/api/items/{id}`
    - Method: `PUT`
    - Headers: `Content-Type: application/json`
    - Body:

        ```json
        {
            "name": "Updated Item",
            "value": 150
        }
        ```

5. **Create a new DELETE request** to delete an item:

    - URL: `http://localhost:8080/api/items/{id}`
    - Method: `DELETE`

