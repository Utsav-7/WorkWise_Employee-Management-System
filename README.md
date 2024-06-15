# WorkWise : Employee Management System

This is a simple Employee Management System built with Spring Boot that supports CRUD operations (Create, Read, Update, Delete).

## Features

- Add a new employee
- Retrieve a list of employees
- Update employee details
- Delete an employee

## Technologies Used

- Java
- Spring Boot
- Spring Security
- Thymeleaf
- MySQL

### Screenshots:
![3](https://github.com/Utsav-7/WorkWise_Employee-Management-System/assets/98468952/ad73ab53-f767-4b91-ad40-810459cabe7c)
![2](https://github.com/Utsav-7/WorkWise_Employee-Management-System/assets/98468952/a8f8d19b-5008-4fe6-8acc-776ec4783119)
![1](https://github.com/Utsav-7/WorkWise_Employee-Management-System/assets/98468952/29ab1505-7e71-4d15-8ccd-1d7e203bcef0)


### Installation

1. Clone the repository:

    ```sh
    git clone https://github.com/yourusername/employee-management-system.git
    cd employee-management-system
    ```

2. Update MySQL database configuration in `src/main/resources/application.properties`:

    ```properties
    spring.datasource.url=jdbc:mysql://localhost:3306/yourdatabase
    spring.datasource.username=yourusername
    spring.datasource.password=yourpassword

    spring.jpa.hibernate.ddl-auto=update
    spring.jpa.show-sql=true
    spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL5Dialect
    ```

3. Build the project using Maven:

    ```sh
    mvn clean install
    ```

4. Run the application:

    ```sh
    mvn spring-boot:run
    ```

## API Endpoints

### Create a new employee

- **URL:** `/api/employees`
- **Method:** `POST`
- **Request Body:**

    ```json
    {
      "firstName": "John",
      "lastName": "Doe",
      "email": "john.doe@example.com",
      "department": "Engineering"
    }
    ```

### Retrieve all employees

- **URL:** `/api/employees`
- **Method:** `GET`

### Retrieve an employee by ID

- **URL:** `/api/employees/{id}`
- **Method:** `GET`

### Update an employee

- **URL:** `/api/employees/{id}`
- **Method:** `PUT`
- **Request Body:**

    ```json
    {
      "firstName": "Jane",
      "lastName": "Doe",
      "email": "jane.doe@example.com",
      "department": "Marketing"
    }
    ```

### Delete an employee

- **URL:** `/api/employees/{id}`
- **Method:** `DELETE`

## Project Structure

```plaintext
employee-management-system
├── src
│   ├── main
│   │   ├── java
│   │   │   └── net
│   │   │       └── javaguide
|   |   |           └── springboot
│   │   │               └── EmployeeManagementWebappApplication
|   |   |               ├── config
│   │   │               │   └── SecurityConfiguration.java
│   │   │               ├── controller
│   │   │               │   └── EmployeeController.java
│   │   │               │   └── MainController.java
│   │   │               │   └── UserRegistrationController.java
│   │   │               ├── model
│   │   │               │   └── Employee.java
│   │   │               │   └── Role.java
│   │   │               │   └── User.java
│   │   │               ├── repository
│   │   │               │   └── EmployeeRepository.java
│   │   │               │   └── UserRepository.java
|   |   |               ├── dto
│   │   │               │   └── UserRegistrationDto.java
│   │   │               └── service
│   │   │                   └── EmployeeService.java
│   │   │                   └── EmployeeServiceImpl.java
│   │   │                   └── UserService.java
│   │   │                   └── UserServiceImpl.java
│   │   └── resources
│   │       ├── templates
│   │       |   └── index.html
│   │       │   └── login.html
│   │       │   └── registration.html
│   │       │   └── new_employee.html
│   │       │   └── update_employee.html
│   │       └── application.properties
|   |
|   |
│   └── test
│       └── java
│           └── net
│               └── javaguide
|                   └── springboot
│                       └── EmployeeManagementApplicationTests.java
├── .gitignore
├── mvnw
├── mvnw.cmd
├── pom.xml
└── README.md
