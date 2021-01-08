# docker-dev

This is my docker-compose used to develop my applications.

## Contents

- postgres 
- redis
- mysql
- mongo

## Usage

After clone the repository, access the directory: docker-dev.

Execute the command:

```script
$ docker-compose up -d
```

You can run only one app or as many as you want:


```script
$ docker-compose up -d postgres mongo
```

To stop

```script
$ docker-compose stop
```

## Examples

### Postgres

To connect to server:

- host: *localhost* or IP of your computer
- port: 5432
- user: postgres
- password: *empty*

If you are using Spring:

```json
spring:
  datasource:
    url: jdbc:postgresql://localhost:5432/<your database name>
    username: postgres
    password:
```

### Redis

- host: *localhost*
- port: 6379

If you are using for cache with Spring:

```json
spring:
  cache:
    type: redis
  redis:
    host: localhost
    port: 6379
```

### Mysql

- host: *localhost*
- port: 3306
- user: admin
- password: *empty*

### Mongo

- host: *localhost*
- port: 27017


```json
spring:
  data:
    mongodb:
      host: mongo
      port: 27017
      database: <your database name>
```
