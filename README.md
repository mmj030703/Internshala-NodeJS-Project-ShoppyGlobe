# Shoppy Globe - Backend

Welcome to the backend of **Shoppy Globe**, an e-commerce platform designed to provide seamless shopping experiences. This backend handles user registration and login, product management and cart operations.

## Features

- **User Authentication**: Secure user registration and login with password hashing.
- **Product Management**: CRUD operations for products.
- **Cart Management**: Add, update, and delete items from the cart.
- **Order Management**: Place and track orders.
- **Middleware**: Centralized error handling and authentication using JWT.
- **Database**: MongoDB for data storage.

---

## Getting Started

### Prerequisites

Ensure you have the following installed:

- [Node.js](https://nodejs.org/) (v14 or later)
- [MongoDB](https://www.mongodb.com/try/download/community) (local or hosted instance)

---

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/shoppy-globe-backend.git
   cd shoppy-globe-backend
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Create a `.env` file in the root directory and add the following variables:

   ```env
   PORT=5000
   MONGO_URI=<your_mongodb_connection_string>
   JWT_SECRET=<your_secret_key>
   ```

4. Start the server:
   ```bash
   npm start
   ```
   The server will run on `http://localhost:5000`.

---

## API Endpoints

### Users

| Method | Endpoint          | Description         |
| ------ | ----------------- | ------------------- |
| POST   | `/users/register` | Register a new user |
| POST   | `/users/login`    | Login a user        |

### Products

| Method | Endpoint        | Description            |
| ------ | --------------- | ---------------------- |
| GET    | `/products`     | Get all products       |
| POST   | `/products`     | Add a new product      |
| PUT    | `/products/:id` | Update a product by ID |
| DELETE | `/products/:id` | Delete a product by ID |

### Cart

| Method | Endpoint           | Description                  |
| ------ | ------------------ | ---------------------------- |
| GET    | `/cart`            | Get cart items for a user    |
| POST   | `/cart/add`        | Add an item to the cart      |
| PUT    | `/cart/update/:id` | Update an item in the cart   |
| DELETE | `/cart/delete/:id` | Remove an item from the cart |

---

## Project Structure

```plaintext
shoppy-globe-backend/
├── config/            # Configuration files
├── controllers/       # Route handlers
├── middleware/        # Custom middleware
├── models/            # Mongoose models
├── routes/            # API routes
├── utils/             # Helper functions
├── server.js          # Entry point
└── .env               # Environment variables
```

---

## Dependencies

- **Express**: Web framework
- **Mongoose**: MongoDB ODM
- **Bcrypt**: Password hashing
- **jsonwebtoken**: Token-based authentication
- **Dotenv**: Environment variable management

---

## Contributing

1. Fork the repository.
2. Create a feature branch: `git checkout -b feature-name`.
3. Commit your changes: `git commit -m 'Add some feature'`.
4. Push to the branch: `git push origin feature-name`.
5. Open a pull request.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---
