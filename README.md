# Running the Application

Follow these steps to set up and run the Java Spring Boot Application (`blinkid-spring-bootapp-main`).

## Prerequisites

Before you begin, ensure you have the following installed on your machine:

- [Java Development Kit (JDK) 11 or higher](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
- [Maven](https://maven.apache.org/install.html)
- [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
- An IDE or text editor (e.g., IntelliJ IDEA, Eclipse, VS Code)

## Step-by-Step Guide

### 1. Clone the Repository

Open a terminal or command prompt and clone the repository using Git:

```bash
git clone https://github.com/your-username/blinkid-spring-bootapp-main.git
```

### 2. Navigate to the Project Directory

Change to the project directory:

```bash
cd blinkid-spring-bootapp-main
```

### 3. Configure the Application

#### 3.1 Database Configuration

Ensure your AWS RDS PostgreSQL database is set up and accessible. Then, configure the application to connect to your database. Open the `application.properties` or `application.yml` file (located in `src/main/resources`) and update the following properties with your database credentials:

For `application.properties`:

```properties
spring.datasource.url=jdbc:postgresql://your-db-endpoint:5432/your-database
spring.datasource.username=your-db-username
spring.datasource.password=your-db-password
spring.jpa.hibernate.ddl-auto=update
```

For `application.yml`:

```yaml
spring:
  datasource:
    url: jdbc:postgresql://your-db-endpoint:5432/your-database
    username: your-db-username
    password: your-db-password
  jpa:
    hibernate:
      ddl-auto: update
```

### 4. Build the Application

Build the application using Maven. Run the following command in the terminal:

```bash
mvn clean install
```

### 5. Run the Application

After building the application, you can run it using the following command:

```bash
mvn spring-boot:run
```

Alternatively, if you prefer to run the JAR file directly:

1. Navigate to the `target` directory:

    ```bash
    cd target
    ```

2. Run the JAR file:

    ```bash
    java -jar blinkid-spring-bootapp-main-0.0.1-SNAPSHOT.jar
    ```

### 6. Verify the Application

Once the application is running, verify it by accessing the following URL in your web browser:

```
http://localhost:8080
```

You should see the application’s homepage or API documentation if configured.

### 7. Access the Application Endpoints

Refer to the API documentation or source code to access various endpoints provided by the application for user operations, authentication, and more.

## Conclusion

You have successfully set up and run the Java Spring Boot Application. For further customization or deployment, refer to the additional documentation and resources available in the repository.
