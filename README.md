## 🔧 Full CRUD Commands (PowerShell)

These commands demonstrate how to perform **Create, Read, Update, and Delete (CRUD)** operations for all main entities using **PowerShell** and a **Spring Boot RESTful API**.

> **Base URL:** `http://localhost:8080`  

```powershell
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
