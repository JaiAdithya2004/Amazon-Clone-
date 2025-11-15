# 🛒 Amazon Clone - Full Stack E-Commerce Application

<div align="center">

![Flutter](https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white)
![Express.js](https://img.shields.io/badge/Express.js-404D59?style=for-the-badge)
![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white)
![Dart](https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white)

**A feature-rich, cross-platform e-commerce application inspired by Amazon**

[Features](#-features) • [Installation](#-installation) • [Tech Stack](#-tech-stack) • [API Documentation](#-api-documentation) 

</div>

---

## 📋 Table of Contents

- [About](#-about-the-project)
- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Architecture](#-architecture)
- [Installation](#-installation)
- [Usage](#-usage)
- [API Documentation](#-api-documentation)
- [Project Structure](#-project-structure)



---

## 🎯 About The Project

This is a **full-stack e-commerce application** built with Flutter and Node.js, replicating core Amazon functionalities. It demonstrates modern mobile development practices, RESTful API design, and real-world e-commerce features including user authentication, product management, shopping cart, order processing, and an admin dashboard.

### Why This Project?

- 🚀 **Production-Ready**: Built with scalability and security in mind
- 📱 **Cross-Platform**: Single codebase runs on iOS, Android, Web, and Desktop
- 🔐 **Secure**: JWT authentication, password hashing, role-based access control
- 💳 **Payment Integration**: Google Pay and Apple Pay support
- 📊 **Analytics Dashboard**: Real-time sales tracking and insights
- ☁️ **Cloud Storage**: Cloudinary integration for efficient image management

---

## ✨ Features

### Customer Features
- 🔐 **User Authentication** - Secure signup/login with JWT tokens
- 🏠 **Product Browsing** - Carousel display, category filtering, search functionality
- 🛍️ **Shopping Cart** - Add/remove products, real-time price calculation
- ⭐ **Product Reviews** - Rate and review purchased products
- 📦 **Order Management** - Place orders, track order status
- 💳 **Payment Integration** - Google Pay & Apple Pay support
- 📍 **Address Management** - Save and manage delivery addresses
- 🔍 **Advanced Search** - Search products by name with instant results

### Admin Features
- ➕ **Product Management** - Add, edit, delete products
- 📊 **Sales Analytics** - View total earnings and category-wise breakdown
- 📋 **Order Management** - View all orders, update order status
- 📈 **Dashboard Charts** - Visual representation of sales data
- 🎯 **Deal of the Day** - Highlight top-rated products



---

## 🛠 Tech Stack

### Frontend
| Technology | Purpose |
|------------|---------|
| **Flutter** | Cross-platform UI framework |
| **Dart** | Programming language |
| **Provider** | State management |
| **HTTP** | API communication |
| **Shared Preferences** | Local data persistence |
| **Carousel Slider** | Image carousel |
| **FL Chart** | Analytics visualization |
| **Cloudinary Public** | Image uploads |

### Backend
| Technology | Purpose |
|------------|---------|
| **Node.js** | JavaScript runtime |
| **Express.js** | Web framework |
| **MongoDB** | NoSQL database |
| **Mongoose** | MongoDB ODM |
| **JWT** | Authentication |
| **bcryptjs** | Password hashing |
| **Nodemon** | Development auto-reload |

---

## 🏗 Architecture

```
┌─────────────────────────────────────────────────────────┐
│                 Flutter Frontend (Client)               │
│           iOS • Android • Web • Desktop                 │
├─────────────────────────────────────────────────────────┤
│                    REST API Layer                       │
│                 (HTTP/JSON Communication)               │
├─────────────────────────────────────────────────────────┤
│              Express.js Backend Server                  │
│  ┌───────────────────────────────────────────────┐    │
│  │  Routes  │  Controllers  │  Middleware        │    │
│  │  • Auth  │  • Products   │  • JWT Verify      │    │
│  │  • Admin │  • Orders     │  • Admin Check     │    │
│  │  • User  │  • Cart       │  • Error Handler   │    │
│  └───────────────────────────────────────────────┘    │
├─────────────────────────────────────────────────────────┤
│                   MongoDB Database                      │
│          Collections: Users, Products, Orders           │
└─────────────────────────────────────────────────────────┘
```

---

## 🚀 Installation

### Prerequisites

Before you begin, ensure you have the following installed:

- **Flutter SDK** (^3.5.4) - [Install Flutter](https://flutter.dev/docs/get-started/install)
- **Node.js** (^18.0.0) - [Download Node.js](https://nodejs.org/)
- **MongoDB** - [MongoDB Atlas](https://www.mongodb.com/cloud/atlas) or local installation
- **Git** - [Download Git](https://git-scm.com/downloads)

### Clone the Repository

```bash
git clone https://github.com/yourusername/amazon-clone.git
cd amazon-clone
```

### Backend Setup

1. **Navigate to server directory:**
```bash
cd server
```

2. **Install dependencies:**
```bash
npm install
```

3. **Create environment file:**
```bash
# Create a .env file in the server directory
touch .env
```

4. **Add environment variables to `.env`:**
```env
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_super_secret_jwt_key_here
PORT=3000
NODE_ENV=development
```

5. **Start the server:**
```bash
# Development mode with auto-reload
npm run dev

# Production mode
npm start
```

The server will run on `http://localhost:3000`

### Frontend Setup

1. **Navigate back to project root:**
```bash
cd ..
```

2. **Install Flutter dependencies:**
```bash
flutter pub get
```

3. **Update API endpoint:**

Open `lib/constants/global_variables.dart` and update the URI:
```dart
static const uri = 'http://localhost:3000'; // For local development
// static const uri = 'https://your-production-url.com'; // For production
```

4. **Run the application:**

```bash
# Run on connected device/emulator
flutter run

# Run on Chrome (Web)
flutter run -d chrome

# Run on specific platform
flutter run -d windows
flutter run -d macos
flutter run -d linux
```

---

## ⚙️ Configuration

### Environment Variables

Create a `.env` file in the `server/` directory:

```env
# Database
MONGO_URI=mongodb+srv://username:password@cluster.mongodb.net/amazon-clone?retryWrites=true&w=majority

# Authentication
JWT_SECRET=your_jwt_secret_key_minimum_32_characters

# Server
PORT=3000
NODE_ENV=development

# Cloudinary (Optional - for image uploads)
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret
```

### MongoDB Setup

**Option 1: MongoDB Atlas (Cloud)**
1. Create account at [MongoDB Atlas](https://www.mongodb.com/cloud/atlas)
2. Create a new cluster
3. Get connection string
4. Whitelist your IP address
5. Create database user

**Option 2: Local MongoDB**
```bash
# Install MongoDB locally
# macOS
brew install mongodb-community

# Start MongoDB
brew services start mongodb-community

# Connection string
mongodb://localhost:27017/amazon-clone
```

---

## 📖 Usage

### Running Tests

```bash
# Flutter tests
flutter test

# Backend tests (if implemented)
cd server && npm test
```

### Building for Production

```bash
# Android APK
flutter build apk --release

# iOS IPA (requires macOS)
flutter build ios --release

# Web
flutter build web

# Windows
flutter build windows

# macOS
flutter build macos
```

---

## 📚 API Documentation

### Authentication Endpoints

#### Sign Up
```http
POST /api/signup
Content-Type: application/json

{
  "name": "John Doe",
  "email": "john@example.com",
  "password": "securePassword123"
}
```

#### Sign In
```http
POST /api/signin
Content-Type: application/json

{
  "email": "john@example.com",
  "password": "securePassword123"
}
```

#### Validate Token
```http
POST /api/tokenIsValid
Headers: x-auth-token: <JWT_TOKEN>
```

### Product Endpoints

#### Get Products by Category
```http
GET /api/products?category=Electronics
```

#### Search Products
```http
GET /api/products/search/:name
```

#### Rate Product
```http
POST /api/rate-product
Headers: x-auth-token: <JWT_TOKEN>
Content-Type: application/json

{
  "id": "product_id",
  "rating": 4.5
}
```

#### Deal of the Day
```http
GET /api/deal-of-day
```

### User Endpoints

#### Add to Cart
```http
POST /api/add-to-cart
Headers: x-auth-token: <JWT_TOKEN>
Content-Type: application/json

{
  "id": "product_id"
}
```

#### Remove from Cart
```http
DELETE /api/remove-from-cart/:id
Headers: x-auth-token: <JWT_TOKEN>
```

#### Save Address
```http
POST /api/save-user-address
Headers: x-auth-token: <JWT_TOKEN>
Content-Type: application/json

{
  "address": "123 Main St, City, Country"
}
```

#### Create Order
```http
POST /api/order
Headers: x-auth-token: <JWT_TOKEN>
Content-Type: application/json

{
  "cart": [...],
  "totalPrice": 999.99,
  "address": "123 Main St, City, Country"
}
```

#### Get User Orders
```http
GET /api/orders/me
Headers: x-auth-token: <JWT_TOKEN>
```

### Admin Endpoints

#### Add Product
```http
POST /admin/add-product
Headers: x-auth-token: <ADMIN_JWT_TOKEN>
Content-Type: application/json

{
  "name": "Product Name",
  "description": "Product Description",
  "images": ["url1", "url2"],
  "quantity": 100,
  "price": 99.99,
  "category": "Electronics"
}
```

#### Get All Products
```http
GET /admin/get-products
Headers: x-auth-token: <ADMIN_JWT_TOKEN>
```

#### Delete Product
```http
POST /admin/delete-product
Headers: x-auth-token: <ADMIN_JWT_TOKEN>
Content-Type: application/json

{
  "id": "product_id"
}
```

#### Get All Orders
```http
GET /admin/get-orders
Headers: x-auth-token: <ADMIN_JWT_TOKEN>
```

#### Change Order Status
```http
POST /admin/change-order-status
Headers: x-auth-token: <ADMIN_JWT_TOKEN>
Content-Type: application/json

{
  "id": "order_id",
  "status": 1
}
```

#### Analytics
```http
GET /admin/analytics
Headers: x-auth-token: <ADMIN_JWT_TOKEN>
```

---

## 📁 Project Structure

```
amazon-clone/
├── lib/                          # Flutter application source
│   ├── main.dart                 # App entry point
│   ├── router.dart               # Navigation routes
│   ├── common/
│   │   └── widgets/              # Reusable UI components
│   ├── constants/
│   │   ├── global_variables.dart # App constants & API URI
│   │   ├── utils.dart            # Utility functions
│   │   └── error_handling.dart   # Error handling utilities
│   ├── features/
│   │   ├── auth/                 # Authentication feature
│   │   ├── home/                 # Home screen
│   │   ├── product_details/      # Product details
│   │   ├── search/               # Search functionality
│   │   ├── cart/                 # Shopping cart
│   │   ├── address/              # Address management
│   │   ├── order_details/        # Order tracking
│   │   ├── account/              # User account
│   │   └── admin/                # Admin dashboard
│   ├── models/
│   │   ├── user.dart             # User model
│   │   ├── product.dart          # Product model
│   │   ├── order.dart            # Order model
│   │   └── rating.dart           # Rating model
│   └── providers/
│       └── user_provider.dart    # User state management
│
├── server/                       # Backend API
│   ├── index.js                  # Server entry point
│   ├── models/
│   │   ├── user.js               # User schema
│   │   ├── product.js            # Product schema
│   │   ├── order.js              # Order schema
│   │   └── rating.js             # Rating schema
│   ├── routes/
│   │   ├── auth.js               # Auth routes
│   │   ├── admin.js              # Admin routes
│   │   ├── product.js            # Product routes
│   │   └── user.js               # User routes
│   ├── middlewares/
│   │   ├── auth.js               # JWT verification
│   │   └── admin.js              # Admin authorization
│   ├── package.json
│   └── .env.example              # Environment variables template
│
├── assets/                       # Static assets
│   ├── images/                   # App images
│   ├── applepay.json             # Apple Pay config
│   └── gpay.json                 # Google Pay config
│
├── android/                      # Android platform files
├── ios/                          # iOS platform files
├── web/                          # Web platform files
├── windows/                      # Windows platform files
├── macos/                        # macOS platform files
├── linux/                        # Linux platform files
│
├── test/                         # Test files
├── pubspec.yaml                  # Flutter dependencies
├── analysis_options.yaml         # Dart analysis config
└── README.md                     # Project documentation
```

---

## 🔒 Security Features

- ✅ **JWT Authentication** - Secure token-based authentication
- ✅ **Password Hashing** - bcryptjs with salt rounds
- ✅ **Role-Based Access Control** - Admin and user roles
- ✅ **Protected Routes** - Middleware for route protection
- ✅ **Input Validation** - Request validation and sanitization
- ✅ **HTTPS Support** - Secure data transmission
- ⚠️ **Environment Variables** - Sensitive data in `.env` (not in repo)

---


