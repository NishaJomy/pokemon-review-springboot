# pokemon-review-springboot
Review and rate your favorite pokemon (in Spring Boot)
Pokémon Review Spring Boot Project
This is a Spring Boot-based web application for managing and reviewing Pokémon. The project allows you to view, create, update, and delete Pokémon entries.

Table of Contents
Getting Started
Prerequisites
Installation
Usage
Endpoints
Examples
Contributing
License
Getting Started
Prerequisites
Before you begin, ensure you have met the following requirements:

Java Development Kit (JDK) installed

Spring Boot framework installed

MySQL or another compatible database server

Clone this repository to your local machine:

bash
Copy code
git clone https://github.com/your-username/pokemon-review-spring-boot.git
Installation
Create a MySQL database and update the database configuration in application.properties:

properties
Copy code
spring.datasource.url=jdbc:mysql://localhost:3306/your_database_name
spring.datasource.username=your_database_username
spring.datasource.password=your_database_password
Build and run the project:

bash
Copy code
cd pokemon-review-spring-boot
./mvnw spring-boot:run
The application will start on http://localhost:8080.

Usage
Endpoints
GET /api/pokemon: Get a list of Pokémon with optional pagination.
GET /api/pokemon/{id}: Get details of a specific Pokémon by ID.
POST /api/pokemon/create: Create a new Pokémon entry.
PUT /api/pokemon/{id}/update: Update an existing Pokémon entry by ID.
DELETE /api/pokemon/{id}/delete: Delete a Pokémon entry by ID.
Examples
Get a list of Pokémon:

http
Copy code
GET http://localhost:8080/api/pokemon
Create a new Pokémon entry:

http
Copy code
POST http://localhost:8080/api/pokemon/create

Request Body:
{
  "name": "Pikachu",
  "type": "Electric",
  "height": 0.4,
  "weight": 6.0
}
Update an existing Pokémon entry by ID:

http
Copy code
PUT http://localhost:8080/api/pokemon/1/update

Request Body:
{
  "name": "Pikachu",
  "type": "Electric",
  "height": 0.4,
  "weight": 6.0
}
Delete a Pokémon entry by ID:

http
Copy code
DELETE http://localhost:8080/api/pokemon/1/delete
Contributing
Contributions are welcome! Please fork this repository and create a pull request with your changes. If you encounter any issues or have suggestions, feel free to open an issue.

License
This project is licensed under the MIT License - see the LICENSE file for details.


