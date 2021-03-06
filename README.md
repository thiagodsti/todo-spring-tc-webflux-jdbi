# TodoApplication
![CI](https://github.com/thiagodsti/todo-spring-tc-webflux-jdbi/actions/workflows/ci.yaml/badge.svg?branch=main)
[![codecov](https://codecov.io/gh/thiagodsti/todo-spring-tc-webflux-jdbi/branch/main/graph/badge.svg?token=0FW8UXB870)](https://codecov.io/gh/thiagodsti/todo-spring-tc-webflux-jdbi)

This is a simple project with springboot + testcontainers + JDBI + Reactive and Postgres.
Everything here is reactive except for the connection with the database.

## Development

### Requirements

- Java 17
- Postgres

### Frameworks / Technologies

- Springboot
- TestContainers
- Webflux Reactive
- JDBI
- Postgres

### Run

Make sure to have a postgres first
```bash
docker run -d -p 5432:5432 \
    -e POSTGRES_PASSWORD=postgres \
    -e PGDATA=/var/lib/postgresql/data/pgdata \
    postgres
```
or if you want to save the database even when the docker is removed
```bash
docker run -d -p 5432:5432 \
    -e POSTGRES_PASSWORD=postgres \
    -e PGDATA=/var/lib/postgresql/data/pgdata \
    -v ~/demo-flyway:/var/lib/postgresql/data \
    postgres
```
Run the application
```bash
mvn spring-boot:run
```

Swagger: http://localhost:8080/swagger-ui.html

### Tests
```bash
mvn clean verify
```
