# Jpa Spring Data

A REST API built with Spring Boot around 3 JPA entities, using PostgreSQL.

## Tech stack

- Java 11, built with Maven
- Spring Boot 2.1.8.RELEASE
- Spring Web (REST controllers)
- Spring Data JPA (Hibernate)
- Spring Data REST
- Spring Boot Actuator
- Lombok
- PostgreSQL driver
- H2 database
- Database: PostgreSQL (`toystoredb` in `application.properties`)

## Concepts covered

JPA relationships, collections, custom JPQL queries, interfaces.

## Data model

| Entity | Fields |
|---|---|
| `Toy` | code, minAge, maxAge, price, ToysLikedbyCust |
| `customerLikes` | toy, liker |
| `Customer` | Id, Name, BirthDay, ToysLiked |

## Project structure

- `com.jee.tp.serveruser`: ServerUserApplication
- `com.jee.tp.serveruser.Models`: Customer, Toy, customerLikes, toySells
- `com.jee.tp.serveruser.Repositories`: customerLikesRepository, customerRepository, toyCustomRepository, toyCustomRepositoryImp, toyRepository, toySellsRepository
- Tests: 1 test class

## How to run

Requirements: a JDK 11+ and Maven (or the included Maven wrapper).
Create the `toystoredb` database and set your own username and password in `src/main/resources/application.properties`.

```bash
./mvnw spring-boot:run
```

The API then listens on `http://localhost:9855`.

---

Author: [Chaouki Bayoudhi](https://github.com/ChaoukiBayoudhi)
