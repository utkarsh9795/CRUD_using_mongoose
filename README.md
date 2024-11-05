
```markdown
# CRUD Using Mongoose

## Overview

This repository contains a simple CRUD (Create, Read, Update, Delete) application built with Node.js and Mongoose, designed to provide an efficient and straightforward way to manage data in a MongoDB database. The application demonstrates how to perform basic database operations using Mongoose as an Object Data Modeling (ODM) library.

## Features

- Create, Read, Update, and Delete operations on data
- Simple RESTful API design
- Mongoose for MongoDB interaction
- Built-in data validation
- Express framework for handling requests
- JSON response format
- Error handling and logging

## Technologies Used

- **Node.js**: JavaScript runtime for server-side programming
- **Express.js**: Web framework for Node.js
- **Mongoose**: ODM for MongoDB and Node.js
- **MongoDB**: NoSQL database to store data
- **Nodemon**: Tool for automatically restarting the server during development

## Installation

To get a copy of this project up and running on your local machine, follow these steps:

### Prerequisites

- Node.js (v12 or higher)
- MongoDB installed locally or access to a MongoDB Atlas account

### Steps

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/CRUD-using-Mongoose.git
   ```

2. Navigate to the project directory:
   ```bash
   cd CRUD-using-Mongoose
   ```

3. Install the dependencies:
   ```bash
   npm install
   ```

4. Configure your MongoDB connection:
   - Open `config.js` and update the `MONGO_URI` variable with your MongoDB connection string.

5. Start the server:
   ```bash
   npm start
   ```

6. The application should now be running on `http://localhost:3000`.

## API Endpoints

### Create a New Item

- **Endpoint**: `POST /api/items`
- **Request Body**:
  ```json
  {
    "name": "Item Name",
    "description": "Item Description"
  }
  ```
- **Response**:
  - **Success**: `201 Created`
  - **Error**: `400 Bad Request`

### Get All Items

- **Endpoint**: `GET /api/items`
- **Response**:
  - **Success**: `200 OK` with an array of items

### Get a Single Item

- **Endpoint**: `GET /api/items/:id`
- **Response**:
  - **Success**: `200 OK` with the item object
  - **Error**: `404 Not Found`

### Update an Item

- **Endpoint**: `PUT /api/items/:id`
- **Request Body**:
  ```json
  {
    "name": "Updated Item Name",
    "description": "Updated Item Description"
  }
  ```
- **Response**:
  - **Success**: `200 OK` with the updated item object
  - **Error**: `400 Bad Request` or `404 Not Found`

### Delete an Item

- **Endpoint**: `DELETE /api/items/:id`
- **Response**:
  - **Success**: `204 No Content`
  - **Error**: `404 Not Found`

## Usage

You can use tools like Postman or CURL to test the API endpoints. Make sure to set the request method and URL according to the specified endpoints.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any improvements or features you would like to add.

