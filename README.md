# Database Integration CRUD

This project is a simple backend API that demonstrates how to bridge the gap between application logic and permanent storage by implementing a RESTful API connected to an SQLite database.

## Technologies Used
* **Node.js**: Backend JavaScript runtime environment.
* **Express.js**: Web framework for building the API endpoints.
* **SQLite**: Lightweight, file-based database for state persistence.

## Getting Started

### Prerequisites
* Node.js installed on your machine.

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/harishkarthik11/Database-Integration-CRUD.git
   ```
2. Navigate to the project directory:
   ```bash
   cd "Database Integration CRUD"
   ```
3. Install the dependencies:
   ```bash
   npm install
   ```

### Running the Server
Start the development server using:
```bash
node server.js
```
The server will start running on `http://localhost:3000`. 
Upon starting, it will automatically connect to the local SQLite database (`database.sqlite`) and ensure the `users` table is created.

## API Endpoints

The API supports the following CRUD operations on the `users` resource:

| HTTP Method | Endpoint      | Description                          | Data Required in Body       |
|-------------|---------------|--------------------------------------|-----------------------------|
| `POST`      | `/users`      | **Create** a new user                | `{"name": "...", "email": "..."}` |
| `GET`       | `/users`      | **Read** all users                   | None                        |
| `GET`       | `/users/:id`  | **Read** a single user by ID         | None                        |
| `PUT`       | `/users/:id`  | **Update** an existing user by ID    | `{"name": "...", "email": "..."}` |
| `DELETE`    | `/users/:id`  | **Delete** a user by ID              | None                        |

## Example Usage (PowerShell)

**Create a new user:**
```powershell
Invoke-RestMethod -Uri "http://localhost:3000/users" -Method Post -Headers @{"Content-Type"="application/json"} -Body '{"name":"Alice","email":"alice@example.com"}'
```

**Get all users:**
```powershell
Invoke-RestMethod -Uri "http://localhost:3000/users" -Method Get
```
