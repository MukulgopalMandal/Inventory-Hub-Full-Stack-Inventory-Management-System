# Inventory Hub

## Overview

This is a full-stack inventory management system built using React, Flask, and MySQL. It allows users to manage products efficiently through REST APIs and provides summary insights through a dashboard.

---

## Features

* Add new products
* View all products
* Update product information
* Delete products
* Product search functionality
* Dashboard statistics
* RESTful API integration
* Input validation and error handling

---

## Tech Stack & Libraries Used

* **React**
  Frontend library used for building an interactive user interface.

* **Vite**
  Fast build tool used for React development.

* **Flask**
  Lightweight Python framework used to build REST APIs.

* **Flask-SQLAlchemy**
  ORM used to interact with the database using Python objects instead of raw SQL.

* **MySQL**
  Relational database used for storing inventory records.

---

## Project Setup

### 1. Clone the repository

```bash
git clone <your-repo-link>
cd inventory_hub
```

---

### 2. Create virtual environment (recommended)

```bash
python -m venv venv
venv\Scripts\activate
```

---

### 3. Install dependencies

```bash
pip install flask flask-sqlalchemy flask-cors pymysql
```

---

### 4. Run the backend application

```bash
python app.py
```

---

### 5. Run the frontend application

```bash
cd frontend
npm install
npm run dev
```

---

### 6. Open in browser

* Frontend:
  http://localhost:5173

* Backend:
  http://127.0.0.1:5000

---

## API Endpoints

* `/products` → View all products
* `/products` → Add products
* `/products/<id>` → Update products
* `/products/<id>` → Delete products

---

## Dashboard Features

* Total Products
* Total Quantity
* Total Inventory Value
* Product Search

---

## Assumptions

* MySQL is used for persistent storage.
* Product IDs are generated automatically.
* Search functionality is implemented on the frontend.
* No authentication system is implemented.

---

## Sample API Requests & Responses

### 1. Add Product

**Request:**

```json
POST /products
{
  "name": "Laptop",
  "quantity": 10,
  "price": 50000
}
```

**Response:**

```json
{
  "message": "Product added successfully"
}
```

---

### 2. Get Products

**Request:**

```json
GET /products
```

**Response:**

```json
[
  {
    "id": 1,
    "name": "Laptop",
    "quantity": 10,
    "price": 50000
  }
]
```

---

### 3. Update Product

**Request:**

```json
PUT /products/1
{
  "name": "Laptop",
  "quantity": 15,
  "price": 55000
}
```

**Response:**

```json
{
  "message": "Product updated successfully"
}
```

---

### 4. Delete Product

**Request:**

```json
DELETE /products/1
```

**Response:**

```json
{
  "message": "Product deleted successfully"
}
```

---

## Future Improvements

* User Authentication
* Product Categories
* Pagination & filtering
* Export Reports (Excel / PDF)
* Inventory Alerts
* Deployment (Render / Vercel / AWS)

---

## Author

Mukulgopal Mandal
