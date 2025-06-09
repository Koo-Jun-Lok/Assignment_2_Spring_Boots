# 🔧 Full CRUD Commands for Spring Boot REST API

Perform **Create, Read, Update, and Delete (CRUD)** operations on main entities using:

- **Option 1: Postman (GUI)**
- **Option 2: Terminal (IntelliJ IDEA)**

**Base URL:** `http://localhost:8080`

---

## Option 1: Postman Commands
 

| Entity    | Operation      | Method  | Endpoint           | Example: Body (raw JSON)                                                                                         |
|-----------|----------------|---------|--------------------|-------------------------------------------------------------------------------------------------------|
| 🧑‍💼 User | Create         | POST    | `/users                           `example: http://localhost:8080/users           | `{ "username": "admin_ameen", "password": "adminpass", "email": "admin@ameen.com", "role": { "id": 1 } }` |
|           | Read All       | GET     | `/users`           | -                                                                                                     |
|           | Read by ID     | GET     | `/users/1`         | -                                                                                                     |
|           | Update         | PUT     | `/users/1`         | `{ "id": 1, "username": "admin_updated", "password": "adminpass", "email": "updated@ameen.com", "role": { "id": 1 } }` |
|           | Delete         | DELETE  | `/users/1`         | -                                                                                                     |

| Entity    | Operation      | Method  | Endpoint           | Example: Body (raw JSON)                 |
|-----------|----------------|---------|--------------------|--------------------------------|
| 🛡️ Role  | Create         | POST    | `/roles`           | `{ "name": "Admin" }`           |
|           | Read All       | GET     | `/roles`           | -                              |
|           | Read by ID     | GET     | `/roles/1`         | -                              |
|           | Update         | PUT     | `/roles/1`         | `{ "id": 1, "name": "SuperAdmin" }` |
|           | Delete         | DELETE  | `/roles/1`         | -                              |

| Entity    | Operation      | Method  | Endpoint           | Example: Body (raw JSON)                                                                                   |
|-----------|----------------|---------|--------------------|--------------------------------------------------------------------------------------------------|
| 📦 Product| Create         | POST    | `/products`        | `{ "name": "Ameen Kopi 3-in-1", "price": 12.50, "category": { "id": 1 } }`                        |
|           | Read All       | GET     | `/products`        | -                                                                                                |
|           | Read by ID     | GET     | `/products/1`      | -                                                                                                |
|           | Update         | PUT     | `/products/1`      | `{ "id": 1, "name": "Ameen Kopi Premium", "price": 13.00, "category": { "id": 1 } }`              |
|           | Delete         | DELETE  | `/products/1`      | -                                                                                                |

| Entity    | Operation      | Method  | Endpoint           | Example: Body (raw JSON)                  |
|-----------|----------------|---------|--------------------|---------------------------------|
| 🗂️ Category| Create        | POST    | `/categories`      | `{ "name": "Minuman Botol" }`   |
|           | Read All       | GET     | `/categories`      | -                               |
|           | Read by ID     | GET     | `/categories/1`    | -                               |
|           | Update         | PUT     | `/categories/1`    | `{ "id": 1, "name": "Minuman Segar" }` |
|           | Delete         | DELETE  | `/categories/1`    | -                               |

---

## Option 2: Terminal (PowerShell curl commands)

Open your terminal (e.g., IntelliJ Terminal or Windows PowerShell) and run these commands:

```powershell

Example: 
# ----------------------
# 🧑‍💼 User
# ----------------------

# Create User
curl -Uri http://localhost:8080/users -Method POST -Body '{"username":"admin_ameen","password":"adminpass","email":"admin@ameen.com","role":{"id":1}}' -ContentType "application/json"

# Read All Users
curl http://localhost:8080/users

# Read User by ID
curl http://localhost:8080/users/1

# Update User
curl -Uri http://localhost:8080/users/1 -Method PUT -Body '{"id":1,"username":"admin_updated","password":"adminpass","email":"updated@ameen.com","role":{"id":1}}' -ContentType "application/json"

# Delete User
curl -Uri http://localhost:8080/users/1 -Method DELETE


# ----------------------
# 🛡️ Role
# ----------------------

# Create Role
curl -Uri http://localhost:8080/roles -Method POST -Body '{"name":"Admin"}' -ContentType "application/json"

# Read All Roles
curl http://localhost:8080/roles

# Read Role by ID
curl http://localhost:8080/roles/1

# Update Role
curl -Uri http://localhost:8080/roles/1 -Method PUT -Body '{"id":1,"name":"SuperAdmin"}' -ContentType "application/json"

# Delete Role
curl -Uri http://localhost:8080/roles/1 -Method DELETE


# ----------------------
# 📦 Product
# ----------------------

# Create Product
curl -Uri http://localhost:8080/products -Method POST -Body '{"name":"Ameen Kopi 3-in-1","price":12.50,"category":{"id":1}}' -ContentType "application/json"

# Read All Products
curl http://localhost:8080/products

# Read Product by ID
curl http://localhost:8080/products/1

# Update Product
curl -Uri http://localhost:8080/products/1 -Method PUT -Body '{"id":1,"name":"Ameen Kopi Premium","price":13.00,"category":{"id":1}}' -ContentType "application/json"

# Delete Product
curl -Uri http://localhost:8080/products/1 -Method DELETE


# ----------------------
# 🗂️ Category
# ----------------------

# Create Category
curl -Uri http://localhost:8080/categories -Method POST -Body '{"name":"Minuman Botol"}' -ContentType "application/json"

# Read All Categories
curl http://localhost:8080/categories

# Read Category by ID
curl http://localhost:8080/categories/1

# Update Category
curl -Uri http://localhost:8080/categories/1 -Method PUT -Body '{"id":1,"name":"Minuman Segar"}' -ContentType "application/json"

# Delete Category
curl -Uri http://localhost:8080/categories/1 -Method DELETE
```

## Run the project using docker
1. cd path/Assignment_2_Spring_Boots
2. docker-compose up
