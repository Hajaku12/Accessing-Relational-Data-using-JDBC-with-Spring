

```markdown
# Accessing Relational Data using JDBC with Spring

This guide walks you through the process of accessing relational data with Spring.

## What You Will Build

You will build an application that uses Spring’s JdbcTemplate to access data stored in a relational database.

## What You Need

- About 15 minutes
- A favorite text editor or IDE
- Java 17 or later
- Maven 3.5+

You can also import the code straight into your IDE:

- **IntelliJ IDEA**

## Store and Retrieve Data

Spring provides a template class called JdbcTemplate that simplifies working with SQL relational databases and JDBC. The JdbcTemplate handles resource acquisition, connection management, exception handling, and error checking, allowing developers to focus on their tasks.

The `main()` method uses Spring Boot’s `SpringApplication.run()` method to launch an application.

Spring Boot supports H2 (an in-memory relational database engine) and automatically creates a connection. When using `spring-jdbc`, Spring Boot also automatically creates a JdbcTemplate. The `@Autowired JdbcTemplate` field automatically loads and makes it available.

The `Application` class implements Spring Boot’s `CommandLineRunner`, executing the `run()` method after the application context is loaded.

1. Install DDL using the `execute` method of JdbcTemplate.
2. Split a list of strings into firstname/lastname pairs using Java 8 streams.
3. Insert records into the table using the `batchUpdate` method of JdbcTemplate for multiple inserts.
4. Use the `query` method to search the table for records that match criteria, converting each result row into a new Customer object using a Java 8 lambda (or an anonymous interface implementation for Java 7 or earlier).

### Best Practices

- Use `?` for arguments to prevent SQL injection attacks.
- For single insert statements, use the `insert` method of JdbcTemplate. For multiple inserts, use `batchUpdate`.

## Build an Executable JAR

You can run the application from the command line with Maven. To build a single executable JAR file:

1. Run the application: `./mvnw spring-boot:run`
2. Build the JAR file: `./mvnw clean package`
3. Run the JAR file: `java -jar target/gs-relational-data-access-0.1.0.jar`

Building an executable JAR simplifies shipping, versioning, and deploying the service across different environments.

The steps described here create a runnable JAR. You can also build a classic WAR file.

### Expected Output

Upon successful execution, you should see the following output:

![image](https://github.com/Hajaku12/Accessing-Relational-Data-using-JDBC-with-Spring/assets/62758651/91393cfe-df18-433a-9050-10563834d248)


```

