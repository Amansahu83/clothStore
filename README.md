# Cloth Store Application

A full-stack e-commerce application for a cloth store with separate admin and user interfaces.

## Features

### User Features
- Browse products
- Add products to cart
- Place orders
- View order history
- User registration and authentication

### Admin Features
- Add, edit, and delete products
- Upload product images
- Manage inventory
- Admin authentication

## Tech Stack

### Backend
- Node.js with Express.js
- PostgreSQL database
- JWT authentication
- Multer for file uploads
- bcryptjs for password hashing

### Frontend
- Next.js (React framework)
- Tailwind CSS for styling
- Axios for API calls
- Local storage for cart management

## Setup Instructions

### Prerequisites
- Node.js (v14 or higher)
- PostgreSQL database
- npm or yarn

### Backend Setup

1. Navigate to the backend directory:
   ```bash
   cd backend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Set up PostgreSQL database:
   - Create a PostgreSQL database named 'clothstore'
   - Configure environment variables in `.env` file
   - Run migrations and seed data:
     ```bash
     npm run setup
     ```
   
   Or run separately:
   ```bash
   npm run migrate  # Create tables
   npm run seed     # Add sample data
   ```

4. Start the backend server:
   ```bash
   npm run dev
   ```

The backend will run on http://localhost:5000

### Frontend Setup

1. Navigate to the frontend directory:
   ```bash
   cd frontend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm run dev
   ```

The frontend will run on http://localhost:3000

## Default Admin Credentials

- Email: admin@clothstore.com
- Password: password

## API Endpoints

### Authentication
- POST `/api/auth/register` - User registration
- POST `/api/auth/login` - User login

### Products
- GET `/api/products` - Get all products
- GET `/api/products/:id` - Get single product
- POST `/api/products` - Create product (Admin only)
- PUT `/api/products/:id` - Update product (Admin only)
- DELETE `/api/products/:id` - Delete product (Admin only)

### Orders
- POST `/api/orders` - Create order
- GET `/api/orders` - Get user orders

## Project Structure

```
clothstore/
├── backend/
│   ├── config/
│   ├── middleware/
│   ├── routes/
│   ├── uploads/
│   ├── server.js
│   └── database.sql
└── frontend/
    ├── components/
    ├── pages/
    ├── utils/
    └── styles/
```