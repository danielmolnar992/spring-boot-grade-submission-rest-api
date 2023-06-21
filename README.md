# Grade Submission REST API with JWT

## Stack

- Java JDK 11
- Spring Boot v2.7.2
- H2 database
- Auth0 4

## Usage

Find attached the Postman collection in `./postman-collection`.
Run the Spring Boot app, base URL will be: `http://127.0.0.1:8080`.
Access H2 console at: `http://127.0.0.1:8080/h2`.

1. Register as a user and authenticate to get the JWT token.
2. Get registered user by ID.
3. Create and manage students, courses and assign them to each other.
    - User requests, `/student/all` and `/course/<id>` don't require JWT.
    - All others do.
4. Create and maintain grades.
    - Grades can be:  "A+", "A", "A-", "B+", "B", "B-", "C+", "C", "C-", "D+", "D", "D-", "F".
    - In order to assign a grade, you have to enroll the student to the course.

Some students and courses are pre-populated for ease of playing around.
DEBUG is set to True, saving changes will automatically restart it.
