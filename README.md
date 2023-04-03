# Spring Boot 1.0 Essential Training Quick Reference Guide

## 1. Introduction to Spring Boot
- What is Spring Boot?
  - A framework that simplifies the development, deployment, and management of Spring applications.
  - Focuses on convention over configuration.
  - Embeds web servers (Tomcat, Jetty, or Undertow) for easy deployment.
- Key benefits:
  - Quick setup and configuration.
  - Production-ready with minimal effort.
  - Standalone applications.
  - Embedded web server support.
  - Opinionated defaults.

## 2. Setting Up Your Development Environment
- Install Java Development Kit (JDK) 8 or later.
- Install Integrated Development Environment (IDE) of your choice (e.g., IntelliJ, Eclipse).
- Install Maven or Gradle for dependency management and build automation.

## 3. Creating a New Spring Boot Project
- Use Spring Initializr (https://start.spring.io) to generate a project structure.
- Select project options:
  - Project type (Maven/Gradle)
  - Packaging (JAR/WAR)
  - Java version
  - Dependencies
- Import the generated project into your IDE.

## 4. Understanding Spring Boot's Project Structure
- `src/main/java`: Java source files.
- `src/main/resources`: Configuration files and static resources.
- `src/test`: Unit and integration tests.
- `pom.xml` (Maven) or `build.gradle` (Gradle): Project build configuration and dependencies.

## 5. Building RESTful Web Services
- Annotate a class with `@RestController` to create a RESTful web service.
- Use annotations to map HTTP methods to Java methods:
  - `@GetMapping`
  - `@PostMapping`
  - `@PutMapping`
  - `@DeleteMapping`
- Use `@PathVariable` and `@RequestParam` to extract values from URL and query parameters.

## 6. Working with Data and Databases
- Spring Data JPA:
  - Simplifies data access and manipulation.
  - Requires a JPA implementation (e.g., Hibernate) and a database (e.g., H2, MySQL, PostgreSQL).
- Create a data model:
  - Annotate a class with `@Entity`.
  - Define fields and relationships.
- Create a repository interface:
  - Extend `JpaRepository` or `CrudRepository`.
  - Define custom query methods.
- Autowire the repository in a service or controller to use it.

## 7. Configuring Spring Boot
- Use `application.properties` or `application.yml` for configuration.
- Customize properties, such as server port, datasource, logging, etc.
- Use `@Value` to inject property values into fields.
- Use `@ConfigurationProperties` for type-safe configuration.

## 8. Validating and Error Handling
- Use Java Bean Validation with `@Valid` annotation on method parameters.
- Add constraint annotations to model fields (e.g., `@NotNull`, `@Size`, `@Pattern`).
- Create a custom exception class and annotate it with `@ResponseStatus`.
- Use `@ExceptionHandler` to handle exceptions and return custom error responses.

## 9. Securing Your Application
- Spring Security:
  - Auto-configured by default in Spring Boot.
  - Provides authentication and authorization.
- Customize security settings:
  - Create a class extending `WebSecurityConfigurerAdapter`.
  - Override methods to configure authentication and authorization.
- Use `@PreAuthorize` and `@PostAuthorize` for method-level security.

## 10. Testing Your Application
- Write unit tests with JUnit
