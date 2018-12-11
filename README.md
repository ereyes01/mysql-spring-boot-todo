# Sample To Do List web application using Spring Boot and MySQL

A simple Todo list application using Spring Boot with the following options:

- Spring JPA and MySQL for data persistence
- Thymeleaf templae for the rendering.

To build and run the sample from a fresh clone of this repo:

## Configure MySQL

1. Create a database in your MySQL instance.
    - Or locally via `docker run --name todo-mysql -e MYSQL_ROOT_PASSWORD=root -e MYSQL_DATABASE=todo -e MYSQL_USER=todo-app -e MYSQL_PASSWORD=abc123 -p 3306:3306 -d mysql:latest`
2. Update the application.properties file in the `src/main/resources` folder with the URL, username and password for your MySQL instance. The table schema for the Todo objects will be created for you in the database.
    - Or leave it alone to use the docker instance locally


## Build and run the sample

1. `mvn clean package`
3. `java -jar target/TodoDemo-0.0.1-SNAPSHOT.war`
3. Open a web browser to http://localhost:8080

As you add and update tasks in the app you can verify the changes in the database through the MySQL console using simple statements like 
`select * from todo_item`.
