# HROne Backend Intern Task – E-Commerce Backend

This project is a backend service built using **FastAPI** and **MongoDB Atlas**, designed to simulate an e-commerce platform backend like Flipkart or Amazon.

---

## Features

- Create Product (`POST /products`)
- List Products with pagination and filtering (`GET /products`)
- Create Order (`POST /orders`)
- List Orders by user with product details and total calculation (`GET /orders/{user_id}`)
- Fully compliant with HROne assignment requirements
- MongoDB Atlas integration via `.env`

---

## Tech Stack

- Python 3.11+
- FastAPI
- PyMongo
- Uvicorn
- MongoDB Atlas (Free M0 cluster)

---

## Getting Started (Local Setup)

### 1. Clone this repository

```bash
git clone https://github.com/saqulain123/hrone-backend.git
cd hrone-backend
```

### 2. Install Dependencies

- pip install -r requirements.txt


### 3. Create .env file

```bash
MONGODB_URL=mongodb+srv://mohammadsaqulain5:KNcXc3uXdpO5QOb9@cluster0.mbabzsy.mongodb.net/hrone_db?retryWrites=true&w=majority
```

### 4.Run Locally

- uvicorn main:app --reload
- Visit: http://localhost:8000/docs

---

## 📁 Project Structure

```
backend/
├── main.py                 # FastAPI application entry point
├── db.py                   # Database connection and configuration
├── requirements.txt        # Python dependencies
├── README.md              # Project documentation
├── models/                # Pydantic data models
│   ├── product_model.py   # Product-related models
│   └── order_model.py     # Order-related models
└── routes/                # API route handlers
    ├── product_routes.py  # Product endpoints
    └── order_routes.py    # Order endpoints
```

## 💾 Database Schema

### Products Collection
```json
{
    "_id": "ObjectId",
    "name": "T-Shirt",
    "price": 499.0,
    "sizes": [
        {
            "size": "large",
            "quantity": 5
        }
    ]
}
```

### Orders Collection
```json
{
    "_id": "ObjectId",
    "userId": "user123",
    "items": [
        {
            "productId": "product_object_id",
            "qty": 2
        }
    ]
}


## Deployment (Render)

- The application is deployed on Render and accessible at:

```bash
 Live URL: https://hronetask.onrender.com
 Swagger Docs: https://hronetask.onrender.com/docs
 ```
