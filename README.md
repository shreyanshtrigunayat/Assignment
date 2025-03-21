# User Management API

This is a simple RESTful API for managing users, built using **Node.js**, **Express**, and **MongoDB**.

## Features
- Create a user
- Retrieve all users
- Retrieve a single user by ID
- Update a user by ID
- Delete a user by ID
- JSON responses with error handling

## Prerequisites
Ensure you have the following installed:
- [Node.js](https://nodejs.org/)
- [MongoDB](https://www.mongodb.com/)

## Setup Instructions

### 1. Clone the Repository
```sh
git clone https://github.com/yourusername/user-crud-api.git
cd user-crud-api
```

### 2. Install Dependencies
```sh
npm install
```

### 3. Start MongoDB
Make sure MongoDB is running locally. You can start it with:
```sh
mongod
```
Alternatively, use a MongoDB cloud service like MongoDB Atlas.

### 4. Run the Server
```sh
node server.js
```
The server will start on `http://localhost:5000/`.

## API Endpoints

### 1. Create a User
**POST** `/users`

#### Request Body (JSON)
```json
{
  "name": "John Doe",
  "email": "john@example.com",
  "age": 25
}
```

#### Response
```json
{
  "_id": "unique_user_id",
  "name": "John Doe",
  "email": "john@example.com",
  "age": 25
}
```

### 2. Retrieve All Users
**GET** `/users`

#### Response
```json
[
  {
    "_id": "unique_user_id",
    "name": "John Doe",
    "email": "john@example.com",
    "age": 25
  }
]
```

### 3. Retrieve a Single User
**GET** `/users/:id`

#### Response
```json
{
  "_id": "unique_user_id",
  "name": "John Doe",
  "email": "john@example.com",
  "age": 25
}
```

### 4. Update a User
**PUT** `/users/:id`

#### Request Body (JSON)
```json
{
  "name": "John Updated",
  "email": "john.updated@example.com",
  "age": 26
}
```

#### Response
```json
{
  "_id": "unique_user_id",
  "name": "John Updated",
  "email": "john.updated@example.com",
  "age": 26
}
```

### 5. Delete a User
**DELETE** `/users/:id`

#### Response
```json
{
  "message": "User deleted successfully"
}
```

## Error Handling
Errors return a JSON response like:
```json
{
  "error": "User not found"
}
```

## License
This project is open-source and available under the MIT License.

