# 🛍️ ShopSphere - Modern E-Commerce Platform

> A comprehensive full-stack e-commerce solution built with the MERN stack, featuring advanced user authentication, seamless shopping experience, and robust admin management capabilities.

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Node](https://img.shields.io/badge/node-%3E%3D14.0.0-brightgreen)
![React](https://img.shields.io/badge/react-18.x-blue)
![MongoDB](https://img.shields.io/badge/mongodb-latest-green)

## 🌟 Project Overview

ShopSphere is a feature-rich e-commerce platform that combines modern web technologies to deliver an exceptional online shopping experience. Built with scalability and user experience in mind, it offers both customer-facing features and comprehensive admin tools.

### Key Highlights
- 🔒 **Secure Authentication** with OTP verification
- 🛒 **Advanced Shopping Cart** with real-time updates  
- 📱 **Responsive Design** optimized for all devices
- ⚡ **Fast Performance** with optimized loading states
- 🎨 **Modern UI/UX** using Material-UI components
- 🔧 **Admin Dashboard** for complete store management

## 🎯 Core Features

### Customer Experience
- **Smart Product Discovery**: Advanced search and filtering capabilities
- **Personalized Shopping**: Wishlist functionality and product recommendations
- **Secure Checkout**: Multiple payment options (COD, UPI, Cards)
- **Order Tracking**: Real-time order status updates
- **Review System**: Rate and review purchased products
- **Profile Management**: Complete account and address management

### Admin Capabilities  
- **Dashboard Analytics**: Comprehensive business insights
- **Inventory Management**: Add, edit, and manage product catalog
- **Order Processing**: Handle customer orders and shipping
- **User Administration**: Manage customer accounts and permissions
- **Content Management**: Control brands, categories, and reviews

### Technical Excellence
- **JWT Authentication**: Secure token-based user sessions
- **Email Integration**: Automated notifications and OTP delivery
- **Real-time Updates**: Live cart and wishlist synchronization
- **Error Handling**: Comprehensive error management and user feedback
- **SEO Optimized**: Search engine friendly structure

## 🏗️ Technology Architecture

### Frontend Stack
```
React 18.x          → Modern component-based UI library
Redux Toolkit       → Predictable state management
Material-UI v5      → Professional component library
React Router v6     → Client-side routing
Axios              → HTTP client for API communication
React Hook Form    → Efficient form handling
Framer Motion      → Smooth animations and transitions
Lottie React       → High-quality loading animations
```

### Backend Stack
```
Node.js            → JavaScript runtime environment
Express.js         → Fast web application framework
MongoDB            → NoSQL database for scalability
Mongoose           → Elegant MongoDB object modeling
JWT                → JSON Web Token authentication
bcryptjs           → Password hashing and security
Nodemailer         → Email service integration
Morgan             → HTTP request logging
```

## 📂 Project Architecture

```
ShopSphere-MERN/
│
├── 🎨 frontend/
│   ├── public/
│   │   ├── index.html           # Application entry point
│   │   └── favicon.ico
│   │
│   ├── src/
│   │   ├── features/            # Feature-based architecture
│   │   │   ├── auth/           # Authentication logic
│   │   │   ├── products/       # Product management
│   │   │   ├── cart/           # Shopping cart functionality
│   │   │   ├── orders/         # Order management
│   │   │   ├── admin/          # Admin dashboard
│   │   │   └── navigation/     # App navigation
│   │   │
│   │   ├── pages/              # Route components
│   │   ├── components/         # Reusable UI components
│   │   ├── hooks/              # Custom React hooks
│   │   ├── config/             # App configuration
│   │   ├── assets/             # Static resources
│   │   ├── theme/              # Material-UI theming
│   │   └── App.js              # Main application component
│   │
│   └── package.json
│
├── ⚙️ backend/
│   ├── controllers/            # Business logic layer
│   │   ├── Auth.js            # Authentication controller
│   │   ├── Product.js         # Product management
│   │   ├── Cart.js            # Shopping cart logic
│   │   ├── Order.js           # Order processing
│   │   └── User.js            # User management
│   │
│   ├── models/                # Database schemas
│   │   ├── User.js            # User model
│   │   ├── Product.js         # Product model
│   │   ├── Order.js           # Order model
│   │   └── Cart.js            # Cart model
│   │
│   ├── routes/                # API endpoints
│   ├── middleware/            # Custom middleware
│   ├── database/              # Database configuration
│   ├── seed/                  # Database seeding scripts
│   └── index.js               # Server entry point
│
└── 📋 README.md
```

## 🚀 Getting Started

### System Requirements
- **Node.js** v14.0.0 or higher
- **MongoDB** v4.4 or higher  
- **npm** v6.0.0 or higher
- **Git** for version control

### Quick Setup

1. **Clone & Navigate**
   ```bash
   git clone https://github.com/Bilal-Raza-SWE/ShopSphere-MERN.git
   cd ShopSphere-MERN
   ```

2. **Backend Configuration**
   ```bash
   cd backend
   npm install
   ```

3. **Frontend Configuration**  
   ```bash
   cd ../frontend
   npm install
   ```

### Environment Setup

#### Backend Environment (`.env`)
```env
# Database Configuration
MONGO_URI=mongodb://localhost:27017/ShopSphere

# Application Settings
ORIGIN=http://localhost:3000
PRODUCTION=false

# Security Configuration
SECRET_KEY=your-strong-secret-key-here
LOGIN_TOKEN_EXPIRATION=30d
COOKIE_EXPIRATION_DAYS=30

# Email Service (Gmail App Password recommended)
EMAIL=your-email@gmail.com
PASSWORD=your-app-password

# OTP & Reset Configuration
OTP_EXPIRATION_TIME=120000
PASSWORD_RESET_TOKEN_EXPIRATION=2m
```

#### Frontend Environment (`.env`)
```env
# API Configuration
REACT_APP_BASE_URL=http://localhost:8000
```

### Database Initialization

Populate your database with sample data:
```bash
cd backend
npm run seed
```

This creates:
- 📦 Sample product catalog
- 👥 Demo user accounts
- 🏷️ Product categories and brands
- ⭐ Sample reviews and ratings
- 🛒 Test shopping data

**Demo Access:**
- Email: `demo@gmail.com`
- Password: `helloWorld@123`

### Launch Application

**Terminal 1 - Backend Server:**
```bash
cd backend
npm run dev
# 🚀 Server running on http://localhost:8000
```

**Terminal 2 - Frontend App:**
```bash
cd frontend  
npm start
# 🌐 App running on http://localhost:3000
```

## 🔌 API Documentation

### Authentication Endpoints
| Method | Endpoint | Description |
|--------|----------|-------------|
| `POST` | `/auth/signup` | Create new user account |
| `POST` | `/auth/login` | Authenticate user login |
| `POST` | `/auth/verify-otp` | Verify email OTP |
| `POST` | `/auth/resend-otp` | Resend verification OTP |
| `POST` | `/auth/forgot-password` | Request password reset |
| `POST` | `/auth/reset-password` | Reset user password |

### Product Management
| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET` | `/products` | Fetch product catalog |
| `GET` | `/products/:id` | Get specific product |
| `POST` | `/products` | Create product (Admin) |
| `PATCH` | `/products/:id` | Update product (Admin) |
| `DELETE` | `/products/:id` | Remove product (Admin) |

### Shopping Cart
| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET` | `/cart` | Retrieve user cart |
| `POST` | `/cart` | Add item to cart |
| `PATCH` | `/cart/:id` | Update cart quantity |
| `DELETE` | `/cart/:id` | Remove cart item |

### Order Processing
| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET` | `/orders` | Get user orders |
| `POST` | `/orders` | Place new order |
| `PATCH` | `/orders/:id` | Update order status (Admin) |

## 🎨 Design System

### Visual Excellence
- **Typography**: Poppins font family for modern aesthetics
- **Color Palette**: Carefully curated Material Design colors
- **Responsive Grid**: Flexible layouts for all screen sizes
- **Micro-interactions**: Smooth hover effects and transitions
- **Loading States**: Engaging Lottie animations during data fetching

### User Experience
- **Intuitive Navigation**: Clear information architecture
- **Fast Loading**: Optimized asset delivery and lazy loading
- **Accessibility**: WCAG compliant design patterns
- **Mobile-First**: Touch-friendly interface design

## 🔄 State Architecture

Redux Toolkit powers the application state with modular slices:

```javascript
store/
├── authSlice.js        # User authentication state
├── productSlice.js     # Product catalog and filters  
├── cartSlice.js        # Shopping cart management
├── orderSlice.js       # Order processing state
├── wishlistSlice.js    # User wishlist data
└── adminSlice.js       # Admin dashboard state
```

## 🧪 Testing & Demo

### Demo Credentials
```
Customer Account:
Email: demo@gmail.com
Password: helloWorld@123

Admin Account:
Available after seeding database
```

### Sample Data Includes
- 50+ Products across multiple categories
- 5+ Brands with authentic logos
- Customer reviews and ratings
- Order history and tracking data
- Admin analytics dashboard data

## 🤝 Contributing

We welcome contributions! Here's how to participate:

1. **Fork** the repository
2. **Create** your feature branch (`git checkout -b feature/amazing-feature`)
3. **Commit** your changes (`git commit -m 'Add amazing feature'`)
4. **Push** to the branch (`git push origin feature/amazing-feature`)
5. **Open** a Pull Request

### Development Guidelines
- Follow existing code style and patterns
- Write clear commit messages
- Add documentation for new features
- Test your changes thoroughly

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for complete details.

## 🙏 Acknowledgments

Special thanks to the open-source community and these amazing technologies:
- **React Team** for the incredible frontend library
- **Material-UI** for the comprehensive component system
- **MongoDB** for the flexible database solution
- **Express.js** for the robust backend framework
- **Node.js** community for continuous innovation

## 📬 Connect & Support

**Developer**: Bilal Raza  
**Email**: bilalrazaswe@gmail.com  
**Project**: [ShopSphere-MERN](https://github.com/Bilal-Raza-SWE/ShopSphere-MERN)

---

### 🌟 Show Your Support

If this project helped you, please consider giving it a ⭐ on GitHub!

**Built with ❤️ using the MERN Stack**