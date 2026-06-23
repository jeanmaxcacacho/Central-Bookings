### Background

This project is loosely based on the *Central Bookings* final project case for the course CSCI 41 (Information Management) at Ateneo de Manila University.

It has been independently reimplemented and extended as a portfolio project.

### Features (needs rewrite! write for HR not the engineer)
- Implementation of CRUD operations.
- Session and authentication.
- Role-based access and views.

### Technologies
- Frontend
  - HTML
  - CSS
  - JavaScript
- Backend
  - PHP
- Database
  - PostgreSQL

### Database Design

The database is designed around the lifecycle of an event booking system. Organizers create events that are scheduled at venues, while customers
purchase tickets through transactions.

The ERD below illustrates the core entities and their relationships.

![Central Bookings ERD](docs/cb-erd.png)

#### Design Decisions

The following assumptions were made during the design of the database:

1. `CUSTOMER` may purchase multiple tickets across different events to support purchasing for multiple event participants.
2. `TICKET` and `TRANSACTION` are modeled separately, allowing the system to track individual tickets while preserving the transactions they are from.
3. `EVENT` references `VENUE` directly, scheduling conflicts are enforced through constraints at the controller level.
