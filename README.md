# Bookstore-Management-api

The Bookstore Management API is a simple RESTful service built with Go. It provides CRUD operations for managing a collection of books, including creating, reading, updating, and deleting book records.

## Features

- **Create Book**: Add a new book to the bookstore.
- **Get All Books**: Retrieve the list of all books.
- **Get Book by ID**: Fetch details of a specific book by its ID.
- **Update Book**: Update details of an existing book.
- **Delete Book**: Remove a book from the collection.

## Technologies Used

- **Golang**: Programming language used to build the API.
- **Gorilla Mux**: Router for handling HTTP requests.
- **JSON**: Data format for request and response payloads.

## API Endpoints

### 1. Get All Books
- **URL**: `/books`
- **Method**: `GET`
- **Response**:
  ```json
  [
    {
      "ID": 1,
      "Name": "Book Name",
      "Author": "Author Name",
      "Publication": "Publisher"
    }
  ]
  ```

### 2. Get Book by ID
- **URL**: `/books/{bookId}`
- **Method**: `GET`
- **Response**:
  ```json
  {
    "ID": 1,
    "Name": "Book Name",
    "Author": "Author Name",
    "Publication": "Publisher"
  }
  ```

### 3. Create Book
- **URL**: `/books`
- **Method**: `POST`
- **Request Body**:
  ```json
  {
    "Name": "New Book",
    "Author": "New Author",
    "Publication": "New Publisher"
  }
  ```
- **Response**:
  ```json
  {
    "ID": 2,
    "Name": "New Book",
    "Author": "New Author",
    "Publication": "New Publisher"
  }
  ```

### 4. Update Book
- **URL**: `/books/{bookId}`
- **Method**: `PUT`
- **Request Body**:
  ```json
  {
    "Name": "Updated Name",
    "Author": "Updated Author",
    "Publication": "Updated Publisher"
  }
  ```
- **Response**:
  ```json
  {
    "ID": 1,
    "Name": "Updated Name",
    "Author": "Updated Author",
    "Publication": "Updated Publisher"
  }
  ```

### 5. Delete Book
- **URL**: `/books/{bookId}`
- **Method**: `DELETE`
- **Response**:
  ```json
  {
    "message": "Book deleted successfully"
  }
  ```

## Setup Instructions

1. Clone the repository:
   ```bash
   git clone https://github.com/harshal-rembhotkar/bookstore-management-api.git
   ```

2. Navigate to the project directory:
   ```bash
   cd bookstore-management-api
   ```

3. Install dependencies:
   ```bash
   go mod tidy
   ```

4. Run the application:
   ```bash
   go run main.go
   ```

5. Access the API at `http://localhost:9010`
