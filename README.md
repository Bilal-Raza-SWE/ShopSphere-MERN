# 🛍️ ShopSphere - MERN E-commerce Platform

A full-stack MERN (MongoDB, Express.js, React, Node.js) e-commerce application with secure authentication, user/admin functionality, and a modern Material-UI interface.

![ShopSphere Banner](frontend/src/assets/images/banner1.jpg)

## ✨ Features

### 🔐 Authentication & Security
- **User Registration & Login** with email verification
- **OTP-based verification** for account security
- **Password Reset** functionality with email notifications
- **JWT token-based authentication** with secure cookie storage
- **Role-based access control** (User/Admin)

### 🛒 Shopping Experience
- **Product Catalog** with advanced filtering and sorting
- **Search functionality** across products
- **Shopping Cart** with real-time updates
- **Wishlist** for saving favorite products
- **Product Reviews & Ratings** system
- **Order Management** with status tracking
- **Multiple Payment Options** (COD, UPI, Card)

### 👤 User Features
- **User Profile Management**
- **Address Management** (Add/Edit/Delete multiple addresses)
- **Order History** with detailed tracking
- **Review System** (Add/Edit/Delete reviews)
- **Wishlist Management**

### 🔧 Admin Features
- **Admin Dashboard** with analytics
- **Product Management** (Add/Edit/Delete/Restore products)
- **Order Management** with status updates
- **User Management**
- **Brand & Category Management**
- **Review Moderation**

### 📱 UI/UX Features
- **Responsive Design** for all devices
- **Material-UI Components** for modern interface
- **Smooth Animations** with Framer Motion
- **Loading States** with Lottie animations
- **Toast Notifications** for user feedback
- **Progressive Web App** features

## 🛠️ Tech Stack

### Frontend
- **React 18** - UI Library
- **Redux Toolkit** - State Management
- **Material-UI (MUI)** - Component Library
- **React Router** - Navigation
- **Axios** - HTTP Client
- **React Hook Form** - Form Management
- **Framer Motion** - Animations
- **Lottie React** - Loading Animations
- **React Toastify** - Notifications

### Backend
- **Node.js** - Runtime Environment
- **Express.js** - Web Framework
- **MongoDB** - Database
- **Mongoose** - ODM
- **JWT** - Authentication
- **bcrypt** - Password Hashing
- **Nodemailer** - Email Service
- **Morgan** - HTTP Logging
- **CORS** - Cross-Origin Resource Sharing

## 📁 Project Structure

```
ShopSphere-MERN/
├── backend/
│   ├── controllers/          # Business logic
│   │   ├── Auth.js
│   │   ├── Product.js
│   │   ├── Cart.js
│   │   ├── Order.js
│   │   └── ...
│   ├── models/              # Database schemas
│   │   ├── User.js
│   │   ├── Product.js
│   │   ├── Order.js
│   │   └── ...
│   ├── routes/              # API endpoints
│   │   ├── Auth.js
│   │   ├── Product.js
│   │   └── ...
│   ├── middleware/          # Custom middleware
│   │   └── VerifyToken.js
│   ├── seed/               # Database seeding
│   │   ├── seed.js
│   │   └── ...
│   ├── database/           # Database connection
│   │   └── db.js
│   ├── utils/              # Utility functions
│   └── index.js            # Entry point
│
└── frontend/
    ├── public/
    │   └── index.html
    ├── src/
    │   ├── components/      # Reusable components
    │   ├── features/        # Feature-based organization
    │   │   ├── auth/
    │   │   ├── products/
    │   │   ├── cart/
    │   │   ├── admin/
    │   │   └── ...
    │   ├── pages/          # Route components
    │   ├── hooks/          # Custom hooks
    │   ├── assets/         # Static assets
    │   ├── config/         # Configuration files
    │   ├── theme/          # MUI theme
    │   ├── App.js          # Main component
    │   └── index.js        # Entry point
    └── package.json
```

## 🚀 Getting Started

### Prerequisites
- Node.js (v14 or higher)
- MongoDB
- npm or yarn

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/ShopSphere-MERN.git
   cd ShopSphere-MERN
   ```

2. **Backend Setup**
   ```bash
   cd backend
   npm install
   ```

3. **Frontend Setup**
   ```bash
   cd frontend
   npm install
   ```

### Environment Configuration

#### Backend (.env)
```env
PORT=8000
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
JWT_EXPIRES_IN=7d
EMAIL_HOST=smtp.gmail.com
EMAIL_PORT=587
EMAIL_USER=your_email@gmail.com
EMAIL_PASS=your_app_password
ORIGIN=http://localhost:3000
```

#### Frontend (.env)
```env
REACT_APP_BASE_URL=http://localhost:8000
```

### Database Setup

1. **Seed the database with sample data**
   ```bash
   cd backend
   npm run seed
   ```

   This will populate your database with:
   - Sample products, brands, and categories
   - Demo users and addresses
   - Sample reviews and orders
   - Demo login: `demo@gmail.com` / `helloWorld@123`

### Running the Application

1. **Start the backend server**
   ```bash
   cd backend
   npm run dev
   # Server runs on http://localhost:8000
   ```

2. **Start the frontend application**
   ```bash
   cd frontend
   npm start
   # Application runs on http://localhost:3000
   ```

## 📋 API Endpoints

### Authentication
- `POST /auth/signup` - User registration
- `POST /auth/login` - User login
- `POST /auth/verify-otp` - OTP verification
- `POST /auth/resend-otp` - Resend OTP
- `POST /auth/forgot-password` - Password reset request
- `POST /auth/reset-password` - Reset password

### Products
- `GET /products` - Get all products
- `GET /products/:id` - Get product by ID
- `POST /products` - Create product (Admin)
- `PATCH /products/:id` - Update product (Admin)
- `DELETE /products/:id` - Delete product (Admin)

### Cart
- `GET /cart` - Get user cart
- `POST /cart` - Add to cart
- `PATCH /cart/:id` - Update cart item
- `DELETE /cart/:id` - Remove from cart

### Orders
- `GET /orders` - Get user orders
- `POST /orders` - Create order
- `PATCH /orders/:id` - Update order status (Admin)

### Reviews
- `GET /reviews/product/:id` - Get product reviews
- `POST /reviews` - Create review
- `PATCH /reviews/:id` - Update review
- `DELETE /reviews/:id` - Delete review

## 🎨 Design Features

- **Modern UI** with Material Design principles
- **Dark/Light Theme** support
- **Responsive Layout** for mobile, tablet, and desktop
- **Smooth Animations** with Framer Motion
- **Loading States** with custom Lottie animations
- **Custom Scrollbars** hidden for clean look
- **Toast Notifications** for user feedback

## 🔄 State Management

The application uses Redux Toolkit for state management with feature-based slices:
- **Auth Slice** - User authentication state
- **Product Slice** - Product catalog and filters
- **Cart Slice** - Shopping cart management
- **Order Slice** - Order processing
- **Review Slice** - Product reviews
- **Wishlist Slice** - User wishlist

## 🧪 Demo Credentials

After seeding the database, you can use:
- **Email**: `demo@gmail.com`
- **Password**: `helloWorld@123`

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Material-UI for the component library
- MongoDB for the database
- Express.js for the backend framework
- React team for the amazing frontend library
- All contributors and supporters

## 📞 Contact

Your Name - your.email@example.com

Project Link: [https://github.com/yourusername/ShopSphere-MERN](https://github.com/yourusername/ShopSphere-MERN)

---

⭐ Star this repository if you found it helpful!