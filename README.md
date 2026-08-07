# E-books (backend)

This is the backend for my E-books shop project, made for the UIKTP course at FCSE. It's a REST API built with Spring Boot. The backend is in a separate repo: https://github.com/Simonajordanova/e-books

The app is an online bookshop. Users can register, log in, browse books and authors and add books to a shopping cart. Admin users can also add, edit and delete books and authors.

## Technologies

- Java 21, Spring Boot 3
- Spring Security with JWT for authentication
- Spring Data JPA / Hibernate
- PostgreSQL
- Lombok

## Endpoints

- `/api/auth` - register and login (login returns a JWT token)
- `/api/books` - get all books, get by isbn, filter by genre or author, add/edit/delete
- `/api/authors` - get all authors, get by id, add/edit/delete
- `/api/shopping-cart` - cart contents, add/remove book, change quantity, clear cart
- `/api/users` - get, edit and delete users

## How to run

You need Java 21 and PostgreSQL installed.

1. Create a database called `uiktpdb` (the connection settings are in `src/main/resources/application-prod.properties`, change the username/password if yours are different)
2. Run:

```
./mvnw spring-boot:run
```

The API starts on http://localhost:8080. The tables are created automatically by Hibernate.

To use the app with the UI, run the backend from the other repo, it starts on http://localhost:3000.


