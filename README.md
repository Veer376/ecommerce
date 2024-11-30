# E-Commerce Web Application

A full-stack e-commerce platform built with the MERN stack (MongoDB, Express, React, Node.js).

## 🛍️ Features

- User authentication (signup, login, password reset)
- Role-based authorization (admin, user)
- Product catalog with categories
- Advanced product filtering and search
- Shopping cart functionality
- Order processing and history
- Admin dashboard for product, order, and user management
- Responsive UI for all devices

## 🚀 Tech Stack

### Backend
- Node.js
- Express.js
- MongoDB with Mongoose
- JWT for authentication
- Bcrypt for password hashing

### Frontend
- React.js
- React Router for navigation
- Context API for state management
- Bootstrap for responsive design
- React Icons

## 📋 Prerequisites

Before running this application, make sure you have the following installed:
- Node.js (v14 or above)
- MongoDB (local or Atlas)
- npm or yarn

## 🔧 Installation & Setup

1. **Clone the repository**
   ```
   git clone https://github.com/Veer376/ecommerce.git
   cd ecommerce-app-2023
   ```

2. **Environment Variables**
   
   Create a `.env` file in the root directory with the following variables:
   ```
   PORT=8080
   DEV_MODE=development
   MONGO_URL=your-mongodb-connection-string
   JWT_SECRET=your-jwt-secret-key
   ```

3. **Install Backend Dependencies**
   ```
   npm install
   ```

4. **Install Frontend Dependencies**
   ```
   cd client
   npm install
   cd ..
   ```

5. **Run the Application**

   For development (run both frontend & backend):
   ```
   npm run dev
   ```

   Run backend only:
   ```
   npm run server
   ```

   Run frontend only:
   ```
   cd client
   npm start
   ```

## 📱 Application Structure

```
├── client/                 # React frontend
│   ├── public/             # Static files
│   └── src/                # React source files
│       ├── components/     # Reusable components
│       ├── context/        # Context providers
│       ├── pages/          # Page components
│       └── App.js          # Main app component
├── config/                 # Configuration files
├── controllers/            # Request handlers
├── helpers/                # Helper functions
├── middlewares/            # Express middlewares
├── models/                 # Mongoose models
├── routes/                 # API routes
└── server.js              # Express app entry point
```

## 🔐 API Endpoints

### Auth Routes
- `POST /api/v1/auth/register` - Register a new user
- `POST /api/v1/auth/login` - Login user
- `GET /api/v1/auth/test` - Protected route test (requires authentication)

### User Routes
- `GET /api/v1/user/profile` - Get user profile
- `PUT /api/v1/user/update` - Update user profile
- `GET /api/v1/user/orders` - Get user orders

### Product Routes
- `GET /api/v1/products` - Get all products
- `GET /api/v1/products/:id` - Get single product
- `POST /api/v1/products` - Create product (admin)
- `PUT /api/v1/products/:id` - Update product (admin)
- `DELETE /api/v1/products/:id` - Delete product (admin)

### Category Routes
- `GET /api/v1/categories` - Get all categories
- `GET /api/v1/categories/:id` - Get single category
- `POST /api/v1/categories` - Create category (admin)
- `PUT /api/v1/categories/:id` - Update category (admin)
- `DELETE /api/v1/categories/:id` - Delete category (admin)

### Order Routes
- `POST /api/v1/orders` - Create order
- `GET /api/v1/orders` - Get all orders (admin)
- `GET /api/v1/orders/:id` - Get single order
- `PUT /api/v1/orders/:id` - Update order status (admin)

## 🚧 Future Improvements

- Payment gateway integration
- Email notifications
- Product reviews and ratings
- Wishlist functionality
- Social media login
- Advanced analytics dashboard

## 📝 License

This project is licensed under the MIT License.
