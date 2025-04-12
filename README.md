JWT Authentication Project
This is a Spring Boot application that demonstrates JWT-based authentication and role-based authorization. It integrates JWT with Spring Security to secure RESTful APIs and uses H2 and MySQL databases for data persistence.

Features:
JWT-based Authentication

Role-based Authorization

Spring Security integration

Data persistence with H2 and MySQL databases

Example user authentication and authorization

Technologies Used:
Java 17

Spring Boot (3.x)

Spring Security

JWT (JSON Web Token)

H2 Database (for development/testing)

MySQL Database (for production)

Lombok (for reducing boilerplate code)

Maven (for build automation)

Setup Instructions:
Prerequisites:
Java 17 or above

Maven 3.9.9 or above

MySQL (for production setup)

IDE (e.g., IntelliJ IDEA, Eclipse)

1. Clone the repository:
2. 
git clone https://github.com/yourusername/jwtauthenticationproject.git
cd jwtauthenticationproject
3. Install dependencies:

mvn clean install
4. Configure Database (if using MySQL):
In application.properties, change the MySQL database URL, username, and password.
properties
spring.datasource.url=jdbc:mysql://localhost:3306/yourdbname
spring.datasource.username=yourusername
spring.datasource.password=yourpassword



4. Run the application:
mvn spring-boot:run


5. Accessing the API:
Access the API via http://localhost:8080

The /user endpoint is protected and requires a JWT token for access.

6. API Example:
To authenticate, send a POST request to /authenticate with your username and password. The response will contain a JWT token.
{
  "username": "user1",
  "password": "password"
}


7. Roles:
USER: Standard user access
ADMIN: Admin privileges for managing users and other resources

License:
This project is licensed under the MIT License - see the LICENSE file for details.
