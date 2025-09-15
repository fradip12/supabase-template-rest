# Supabase Learning Project - REST API Template

A Node.js Express REST API demonstrating CRUD operations with Supabase as the backend database. This project serves as a learning template for integrating Supabase with a Node.js application.

## 📋 Overview

This project implements a simple products API with full CRUD (Create, Read, Update, Delete) functionality using:
- **Express.js** - Web framework for Node.js
- **Supabase** - Backend-as-a-Service for database operations
- **Morgan** - HTTP request logger middleware
- **dotenv** - Environment variable management

## 🚀 Features

- ✅ Get all products
- ✅ Get a specific product by ID
- ✅ Create new products
- ✅ Update existing products
- ✅ Delete products
- ✅ Request logging with Morgan
- ✅ Environment variable configuration

## 📦 Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd supabase_learn
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   
   Create a `.env` file in the root directory:
   ```env
   SUPABASE_URL=your_supabase_project_url
   SUPABASE_ANON_KEY=your_supabase_anon_key
   ```

4. **Set up Supabase Database**
   
   Create a `products` table in your Supabase database with the following structure:
   ```sql
   CREATE TABLE products (
     id SERIAL PRIMARY KEY,
     name VARCHAR(255) NOT NULL,
     description TEXT,
     price DECIMAL(10,2)
   );
   ```

## 🏃‍♂️ Usage

**Start the development server:**
```bash
npm start
```

The server will start on `http://localhost:3000`

## 📚 API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/` | Welcome message |
| GET | `/products` | Get all products |
| GET | `/products/:id` | Get a specific product |
| POST | `/products` | Create a new product |
| PUT | `/products/:id` | Update a product |
| DELETE | `/products/:id` | Delete a product |

### Example Requests

**Get all products:**
```bash
curl http://localhost:3000/products
```

**Create a new product:**
```bash
curl -X POST http://localhost:3000/products \
  -H "Content-Type: application/json" \
  -d '{"name": "Sample Product", "description": "A sample product", "price": 29.99}'
```

**Update a product:**
```bash
curl -X PUT http://localhost:3000/products/1 \
  -H "Content-Type: application/json" \
  -d '{"name": "Updated Product", "description": "Updated description", "price": 39.99}'
```

**Delete a product:**
```bash
curl -X DELETE http://localhost:3000/products/1
```

## 🛠️ Technologies Used

- **Node.js** - JavaScript runtime
- **Express.js** - Web application framework
- **Supabase** - Backend-as-a-Service
- **Morgan** - HTTP request logger
- **Body-parser** - Parse incoming request bodies
- **dotenv** - Load environment variables

## 📁 Project Structure

```
supabase_learn/
├── app.js              # Main application file
├── package.json        # Project dependencies and scripts
├── README.md          # Project documentation
└── .env               # Environment variables (create this)
```

## 🔧 Configuration

Make sure to configure your Supabase project:

1. Create a new project at [supabase.com](https://supabase.com)
2. Get your project URL and anon key from the API settings
3. Create the `products` table with the required schema
4. Add the credentials to your `.env` file

## 🤝 Contributing

This is a learning project. Feel free to:
- Fork the repository
- Create feature branches
- Submit pull requests
- Report issues

## 📝 License

ISC License

## 🎯 Learning Goals

This project helps you learn:
- Setting up a Node.js Express server
- Integrating Supabase with a Node.js application
- Implementing RESTful API endpoints
- Handling environment variables
- Using middleware for logging and request parsing

---

**Happy Learning! 🚀**