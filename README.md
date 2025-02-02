# Simple REST API in Pure Go

This is a basic REST API built using only Go's standard library, without any external dependencies.

## Features
- `GET /ping` → Returns `pong`
- `GET /users` → Retrieves a list of users
- `POST /users` → Adds a new user

## Setup and Running

### 1. Clone the repository
```sh
git clone <repository-url>
cd <repository-folder>
```

### 2. Initialize a Go module (if not already initialized)
```sh
go mod init myapp
```

### 3. Run the server
```sh
go run main.go
```

## API Endpoints

### Ping Test
**Request:**
```sh
curl -X GET http://localhost:8080/ping
```
**Response:**
```json
{"message": "pong"}
```

### Get Users
**Request:**
```sh
curl -X GET http://localhost:8080/users
```
**Response:**
```json
[
  {"id": 1, "name": "Alice", "age": 25},
  {"id": 2, "name": "Bob", "age": 30}
]
```

### Create a User
**Request:**
```sh
curl -X POST http://localhost:8080/users \
     -H "Content-Type: application/json" \
     -d '{"name":"Charlie", "age":27}'
```
**Response:**
```json
{"id": 3, "name": "Charlie", "age": 27}
```

## Notes
- The server runs on port `8080` by default.
- This project was built for learning purposes to better understand Go's built-in HTTP capabilities.

---

🚀 Happy Coding!
