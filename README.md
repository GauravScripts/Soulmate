# Soulmate Web Application
<hr>
Soulmate is a web application that allows users to connect with potential partners in a way similar to the popular dating app, Tinder. The application was built using Angular and Spring Boot, with data stored in Neo4j, MongoDB, and MySQL databases. Communication between components is facilitated through RabbitMQ.
<img src="https://raw.githubusercontent.com/GauravScripts/Soulmate/main/Screenshot/Screenshot%202023-03-28%20175539.png">
<img src ="https://raw.githubusercontent.com/GauravScripts/Soulmate/main/Screenshot/Screenshot%202023-03-28%20174348.png">
<img src="https://raw.githubusercontent.com/GauravScripts/Soulmate/main/Screenshot/Screenshot%202023-03-28%20175651.png">
Installation
To install Soulmate on your local machine, follow these steps:

Clone the GitHub repository:
bash
Install the necessary dependencies:
bash
cd soulmate

# Install Angular CLI globally if you haven't done so already
npm install -g @angular/cli

# Install npm dependencies for both the frontend and backend
cd frontend
npm install
cd ../backend
npm install
Start the databases:

For Neo4j, download and run the Neo4j Desktop application.
For MongoDB, download and run the MongoDB Community Server.
For MySQL, download and run the MySQL Community Server.
Configure the application.properties file in the backend directory with your database settings:

properties
spring.data.neo4j.uri=bolt://localhost:7687
spring.data.neo4j.username=neo4j
spring.data.neo4j.password=your-neo4j-password

spring.data.mongodb.host=localhost
spring.data.mongodb.port=27017
spring.data.mongodb.database=soulmate

spring.datasource.url=jdbc:mysql://localhost:3306/soulmate
spring.datasource.username=your-mysql-username
spring.datasource.password=your-mysql-password
Start the backend server:
bash
cd backend
./mvnw spring-boot:run
Start the frontend server:
bash
cd frontend
ng serve
Navigate to http://localhost:4200 in your browser to access Soulmate.
Usage
To use Soulmate, follow these steps:

Create an account by clicking on the "Sign up" button and entering your information.
Fill out your profile information and add photos.
Browse through potential matches by swiping left or right.
If you and a match both swipe right on each other, you will be able to message each other through the app.
Contributing
If you would like to contribute to Soulmate, feel free to submit a pull request. Before doing so, please ensure that your code passes all tests and adheres to our coding conventions.

License
Soulmate is licensed under the MIT License.
