<h2>Overview</h2>
A simple server-side web application that allows you to perform all CRUD operations on a list of employees. Employees are in the database and information is transferred using JSON
<br>
<br>
The application allows you to get a list of all employees, a single employee by ID, add a new employee, modify an existing employee and delete an employee
<br>
<br>
When creating the REST API, we adhered to generally accepted standards:
<br>
<br>

| HTTP method  | URL | CRUD operation |
| ------------- | ------------- | ----------- |
| GET  | api/employees  | getting all employees |
| GET  | api/employees/{employeeId}  | getting single employee |
| POST  | api/employees  | adding an employee |
| PUT  | api/employees  | employee updating |
| DELETE  | api/employees/{employeeId}  | employee removal |
<br>
All CRUD operations are performed using interfaces "EmployeeDAO", "EmployeeService" and classes "EmployeeDAOImpl", "EmployeeServiceImpl" that implements these interfaces
<br>
<br>
Class "MyController" is used for calling methods from "EmployeeService" and throwing exceptions
<br>
<br>
Exception handling is implemented in classes "EmployeeGlobalExceptionHandler", "EmployeeIncorrectData" and "NoSuchEmployeeException" of package "exception_handling"
<h3>Configuration</h3>
Project is created from Maven archetype "maven-archetype-webapp"<br>
Deployment to the server is performed by Tomcat<br>
The configuration of Spring Container and database connection is the responsibility of file "MyConfig.java" of package "configuration"<br>

<h3>Testing</h3>
