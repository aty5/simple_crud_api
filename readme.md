# Simple CRUD API

## Description

This is a simple Express.js API with MongoDB using Mongoose. It allows basic CRUD operations for managing products in a database.

## Features

- **GET** `/api/products` - Get all products
- **GET** `/api/products/:id` - Get a product by ID
- **POST** `/api/products` - Create a new product
- **PUT** `/api/products/:id` - Update a product by ID
- **DELETE** `/api/products/:id` - Delete a product by ID

## Requirements

- Node.js (v14 or higher)
- MongoDB account (to create a connection URI)

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/simple-crud-api.git
   ```
2. Navigate to the project directory:
   ```bash
   cd simple-crud-api
   ```
3. Install dependencies:
   ```bash
   npm install
   ```
4. Create a .env file in the root directory and add your MongoDB connection string:
   ```bash
   MONGO_URI=mongodb+srv://your_mongodb_uri_here
   ```
   Note: To get your MongoDB URI, create an account on MongoDB Atlas or set up a local MongoDB server.
   
5. Start the server:
   ```bash
   npm start
   ```
6. The API will be running on http://localhost:3000.

## API Documentation

### GET `/api/products`
Fetch all products.

#### Response
- 200 OK: Returns a list of all products.

### GET `/api/products/:id`
Fetch a product by its ID.

#### Params
- `id`: The product's unique identifier.

#### Response
- 200 OK: Returns the product.
- 404 Not Found: If the product doesn't exist.

### POST `/api/products`
Create a new product.

#### Request Body
- `name` (String): Product name (required)
- `quantity` (Number): Product quantity (default: 0)
- `price` (Number): Product price (default: 0)
- `image` (String, optional): Product image URL

#### Response
- 200 OK: Returns the created product.

### PUT `/api/products/:id`
Update a product by its ID.

#### Params
- `id`: The product's unique identifier.

#### Request Body
- Same as the `POST` request.

#### Response
- 200 OK: Returns the updated product.
- 404 Not Found: If the product doesn't exist.

### DELETE `/api/products/:id`
Delete a product by its ID.

#### Params
- `id`: The product's unique identifier.

#### Response
- 200 OK: Product successfully deleted.
- 404 Not Found: If the product doesn't exist.
