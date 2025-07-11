# Spring Boot API

A simple REST API built with Spring Boot 3.0.0 and Java.

## Project Structure

```
spring-boot-api/
├── .gitignore
├── pom.xml
├── README.md
└── src/
    ├── main/
    │   ├── java/com/example/api/
    │   │   ├── ApiApplication.java          # Main application class
    │   │   └── controller/
    │   │       └── HelloController.java     # REST controller
    │   └── resources/
    │       └── application.properties       # Configuration
    └── test/
        └── java/com/example/api/controller/
            └── HelloControllerTest.java     # Unit tests
```

## Features

- **Spring Boot 3.0.0** - Latest Spring Boot framework
- **Maven** - Build and dependency management
- **REST API** - Three sample endpoints
- **Unit Tests** - Complete test coverage for controllers
- **Git Ready** - Includes .gitignore for Java/Maven projects

## API Endpoints

| Method | Endpoint | Description | Response |
|--------|----------|-------------|----------|
| GET | `/hello` | Basic greeting | "Hello, World!" |
| GET | `/hello/{name}` | Personalized greeting | "Hello, {name}!" |
| GET | `/api/status` | API health check | "API is running successfully!" |

## Prerequisites

- Java 17 or higher
- Maven 3.6 or higher

## Getting Started

### 1. Clone or Download the Project

```bash
git clone <repository-url>
cd spring-boot-api
```

### 2. Build the Project

```bash
mvn clean install
```

### 3. Run the Application

```bash
mvn spring-boot:run
```

The application will start on `http://localhost:8080`

### 4. Test the API

You can test the endpoints using curl, Postman, or any HTTP client:

```bash
# Basic greeting
curl http://localhost:8080/hello

# Personalized greeting
curl http://localhost:8080/hello/John

# API status
curl http://localhost:8080/api/status
```

## Running Tests

Run the unit tests with:

```bash
mvn test
```

## Configuration

The application configuration is in `src/main/resources/application.properties`:

```properties
server.port=8080
spring.application.name=spring-boot-api
```

## Development

### Adding New Endpoints

1. Create or modify controllers in `src/main/java/com/example/api/controller/`
2. Add corresponding tests in `src/test/java/com/example/api/controller/`
3. Run tests to ensure everything works: `mvn test`

### Adding Dependencies

Add new dependencies to `pom.xml` in the `<dependencies>` section.

## Building for Production

Create a JAR file for deployment:

```bash
mvn clean package
```

The JAR file will be created in the `target/` directory.

Run the JAR file:

```bash
java -jar target/api-1.0-SNAPSHOT.jar
```

## Technology Stack

- **Java 17+**
- **Spring Boot 3.0.0**
- **Spring Web** - For REST API
- **Maven** - Build tool
- **JUnit 5** - Testing framework

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests for new functionality
5. Run tests to ensure everything passes
6. Submit a pull request                                                                                                                                                                 