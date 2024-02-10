+++
title = 'Spring Employee System Part 2'
date = 2024-02-10T09:22:22+08:00
draft = false
+++


In Part 2, we introduce steps setting backend Java spring boot project:

[Source code](https://github.com/yennanliu/SpringPlayground/tree/main/springEmployeeSystem)

<!--more-->

1. Clone the Repository:

```bash
git clone https://github.com/yennanliu/SpringPlayground.git
```

2. Navigate to the Backend Directory:
```bash
cd SpringPlayground/springEmployeeSystem/backend
```


3. Choose an IDE:
You can use any Java IDE of your choice such as IntelliJ IDEA, Eclipse, or Spring Tool Suite (STS).

4. Open the Project in Your IDE:
Open the springEmployeeSystem/backend directory in your chosen IDE.

5. Ensure JDK is Installed:
Make sure you have JDK (Java Development Kit) installed on your system. Spring Boot typically requires JDK 8 or later versions.

6. Review Project Structure:
Familiarize yourself with the project structure. You'll find the main source code in the src/main/java directory and resources such as application properties in src/main/resources.

Below is the final project structure:
```
.
├── Dockerfile
├── pom.xml
├── sql
│   └── dml.sql
├── src
│   ├── main
│   │   ├── java
│   │   │   └── EmployeeSystem
│   │   │       ├── EmployeeSystemApplication.java
│   │   │       ├── common
│   │   │       │   └── ApiResponse.java
│   │   │       ├── config
│   │   │       │   ├── MessageStrings.java
│   │   │       │   └── WebConfig.java
│   │   │       ├── controller
│   │   │       │   ├── CheckinController.java
│   │   │       │   ├── DepartmentController.java
│   │   │       │   ├── OptionSchemaController.java
│   │   │       │   ├── TicketController.java
│   │   │       │   ├── UserController.java
│   │   │       │   └── VacationController.java
│   │   │       ├── enums
│   │   │       │   ├── ResponseStatus.java
│   │   │       │   ├── Role.java
│   │   │       │   ├── TicketStatus.java
│   │   │       │   └── VacationStatus.java
│   │   │       ├── exception
│   │   │       │   ├── AuthenticationFailException.java
│   │   │       │   └── CustomException.java
│   │   │       ├── model
│   │   │       │   ├── AuthenticationToken.java
│   │   │       │   ├── Checkin.java
│   │   │       │   ├── Department.java
│   │   │       │   ├── NotificationEmail.java
│   │   │       │   ├── OptionSchema.java
│   │   │       │   ├── Ticket.java
│   │   │       │   ├── User.java
│   │   │       │   ├── Vacation.java
│   │   │       │   └── dto
│   │   │       ├── repository
│   │   │       │   ├── CheckinRepository.java
│   │   │       │   ├── DepartmentRepository.java
│   │   │       │   ├── OptionSchemaRepository.java
│   │   │       │   ├── TicketRepository.java
│   │   │       │   ├── TokenRepository.java
│   │   │       │   ├── UserRepository.java
│   │   │       │   └── VacationRepository.java
│   │   │       ├── service
│   │   │       │   ├── AuthenticationService.java
│   │   │       │   ├── CheckinService.java
│   │   │       │   ├── DepartmentService.java
│   │   │       │   ├── MailContentBuilder.java
│   │   │       │   ├── MailService.java
│   │   │       │   ├── OptionSchemaService.java
│   │   │       │   ├── TicketService.java
│   │   │       │   ├── UserService.java
│   │   │       │   └── VacationService.java
│   │   │       └── util
│   │   │           └── Helper.java
│   │   └── resources
│   │       ├── application.properties
│   │       └── templates
│   │           └── mailTemplate.html
│   └── test
│       └── java
│           └── EmployeeSystem
│               └── EmployeeSystemApplicationTests.java
```


7. Set Up Dependencies:
Check the pom.xml file to ensure all necessary dependencies are included. The project might already have dependencies like Spring Boot Starter Web for building web applications, Spring Data JPA for data access, etc.

8. Configure Application Properties:
Review the src/main/resources/application.properties file to configure any required properties such as database connection details.

9. Start Coding:
Begin coding your backend application logic. You can create controllers under the com.example.demo.controller package, services under com.example.demo.service, and entity classes under com.example.demo.entity.

10. Run the Application:
You can run the Spring Boot application directly from your IDE by running the DemoApplication class, which is typically located under the com.example.demo package. Alternatively, you can use Maven to run the application from the command line:

```bash
mvn spring-boot:run
```
11. Test the Endpoints:
Once the application is running, test the RESTful endpoints using tools like Postman or curl. The endpoints are defined in the controller classes.

12. Explore and Extend:
Explore the existing codebase and extend it according to your requirements. You can add new features, modify existing ones, or refactor the code as needed.

By following these steps, you should be able to set up and start working on the backend Java project for the Spring Employee System. Feel free to reach out if you encounter any issues or need further assistance!