# Simple CRUD Application using Go (Golang), net/http, and MySQL

This is a simple CRUD (Create, Read, Update, Delete) application built using Go (Golang), net/http package for handling HTTP requests, and MySQL for database storage. The application allows you to perform basic CRUD operations on a "users" table.

## Project Setup

1. Install Go: Make sure you have Go installed on your machine.

2. Clone the repository: Use the following command to clone the repository to your local machine.

   ```
   git clone https://github.com/your-username/golang-crud.git
   cd golang-crud
   ```
   
## Install dependencies: 

Run the following command to install the required Go packages.
```
go get -d ./...
```

## Set up the MySQL database: 
Make sure you have a MySQL server installed and running. Create a database with the name "your_database_name" (as mentioned in the code) and set up a user with the appropriate privileges.

## Configure the database connection: 
Update the DBUser, DBPassword, and DBName constants in the main.go file with your MySQL credentials.

## Build and run the application: 
Execute the following command to build and run the Go application.
```
go run main.go
```

## Database Setup
Create the "users" table: The application will automatically create the "users" table with columns id (int) and name (string) when it starts up. No additional setup is needed.

## cURL Commands
You can use cURL or Postman to interact with the application. Here are some example cURL commands for testing the CRUD operations:

### Create a new user:
curl -X POST -d '{"name":"John Doe"}' http://localhost:8080/create

### Read all users:
curl http://localhost:8080/read

### Update a user (replace <user_id> with the ID of the user you want to update):
curl -X PUT -d '{"id":<user_id>,"name":"Updated Name"}' http://localhost:8080/update

### Delete a user (replace <user_id> with the ID of the user you want to delete):
curl -X DELETE -d '{"id":<user_id>}' http://localhost:8080/delete
