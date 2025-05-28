# SpringBoot CRUD JPA Example

This is a demonstration project that implements basic **Create, Read, Update, Delete (CRUD)** operations using **Spring Boot** and **Spring Data JPA**. It is designed as an educational example to showcase the integration of Spring Boot with JPA for managing customer data using an in-memory **H2 database**.

---

## 📚 Overview

This project illustrates core patterns of Spring Boot development, with a focus on:

- Repository-based data access
- Annotation-driven configuration
- Modern enterprise Java practices

The application follows a layered architecture separating persistence, business logic, and orchestration layers.

---

## 🧱 Project Structure & Architecture

The project is composed of the following main components:

- **Infrastructure Layer**
- **Domain Layer**
- **Application Layer**
- **Main Class**: `AccessingDataJpaApplication`
- **Startup Runner**: `CommandLineRunner demo()`
- **Configuration File**: `application.properties`
- **Entity**: `Customer` annotated with `@Entity`
- **Repository**: `CustomerRepository` extends `CrudRepository`

Data operations are powered by **Spring Data JPA** and use the **H2 in-memory database** for persistence.

---

## ⚙️ Technology Stack

| Component        | Technology         | Version       | Purpose                                           |
|------------------|--------------------|---------------|---------------------------------------------------|
| Runtime          | Java               | 17            | Application execution environment                 |
| Framework        | Spring Boot        | 3.5.0         | Application framework and auto-configuration      |
| Data Access      | Spring Data JPA    | Included      | Repository pattern and ORM abstraction            |
| Database         | H2 Database        | Runtime scope | In-memory database for development/demo           |
| Build Tool       | Maven              | 3.9.9         | Dependency management and build automation        |
| Testing          | Spring Boot Test   | Included      | Integration testing framework                     |

> The Maven Wrapper (`mvnw` / `mvnw.cmd`) is included for cross-platform builds without local Maven installation.

---

## 🧩 Core Application Components

This application features a simple layered design:

### Entity & Persistence
- `Customer` class annotated with `@Entity`, `@Id`, `@GeneratedValue`
- Uses H2 for in-memory data persistence

### Repository Layer
- `CustomerRepository` extends `CrudRepository<Customer, Long>`
- Includes built-in CRUD and custom query methods like `findByLastName()`

### Startup & Demo
- The `main()` method in `AccessingDataJpaApplication` initializes the application
- A `CommandLineRunner` bean demonstrates all CRUD operations on startup:
  - `save()`
  - `findAll()`
  - `findById()`
  - `findByLastName()`

---

## 🚀 Application Features

### ✅ Demonstration-Oriented Design
Includes a pre-configured `CommandLineRunner` to automatically showcase CRUD operations on application startup.

### ⚙️ Minimal Configuration
Leverages Spring Boot's auto-configuration:
- No external database setup required
- Uses in-memory H2 by default

### 🌐 Cross-Platform Support
Built-in Maven Wrapper ensures build consistency across OS platforms.

### 🔧 Modern Development Practices
- Annotation-based configuration
- Spring Data JPA repository pattern
- Constructor and field-based dependency injection
- Integration testing via `spring-boot-starter-test`

---

## 📎 Resources & Source Files

- `pom.xml`
- `README.md`
- `src/main/java/...` — Source code for application, entity, repository
- `src/main/resources/application.properties`

---

## 📖 More Information

- **Main Application Class** — `AccessingDataJpaApplication`
- **Customer Entity Model** — Definition and annotations
- **Data Access Layer** — `CustomerRepository` and custom queries

---
# 🧰 SpringBoot CRUD JPA – Local Setup Guide

This document provides **step-by-step instructions** for setting up and running the SpringBoot CRUD JPA application locally. It includes prerequisites, development environment setup, and how to execute and verify the application.

> For details on the app structure, see: **Application Architecture**  
> For build configuration, see: **Build System**

---

## ✅ Prerequisites

Ensure the following components are available in your environment:

| Component     | Required Version | Source                                |
|---------------|------------------|----------------------------------------|
| Java          | 17               | [`pom.xml`](pom.xml#L30)               |
| Maven         | 3.9.9            | `.mvn/wrapper/maven-wrapper.properties` |
| Spring Boot   | 3.5.0            | [`pom.xml`](pom.xml#L8)                |

Verify Java is installed:

```bash
java -version
javac -version


## 📦 How to Run

```bash
./mvnw spring-boot:run
