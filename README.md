# Sync Map App

Sync Map App is an interactive mapping application that provides users with a seamless experience for exploring geographical locations. It integrates OpenStreetMap and offers JWT-based authentication to ensure secure access.

## Features

- 🗺️ **Interactive Maps** - View and explore locations dynamically.
- 🔐 **JWT Authentication** - Secure login and session management.
- 📍 **State-wise Data** - Displays tourist visitor counts and images for different states.
- 🚀 **Fast & Responsive** - Built with React.js, Node.js, and Express.js.

## Tech Stack

- **Frontend:** React.js, Bootstrap, OpenStreetMap
- **Backend:** Node.js, Express.js
- **Database:** SQLite3 (storing state-wise data)
- **Authentication:** JWT (JSON Web Tokens)

## Database Schema
The application stores user and state data using the following database schema:

**users Table**
```bash
CREATE TABLE users (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    username TEXT UNIQUE NOT NULL,
    email TEXT NOT NULL,
    password TEXT NOT NULL
);
```

**states Table**
```bash
CREATE TABLE states (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    name TEXT UNIQUE NOT NULL,
    tourist_visitors_count INTEGER NOT NULL,
    latitude REAL NOT NULL,
    longitude REAL NOT NULL,
    image_url TEXT NOT NULL
);
```

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yesuballa/sync-map-app.git
   cd sync-map-app
   ```

2. Set up backend:
   ```bash
   cd sync-map-backend
    npm install
    nodemon app.js
   ```

3. Set up the frontend:
   ```bash
   cd ../sync-map-frontend
    npm install
    npm start
   ```

4. Open the app in your browser at `http://localhost:3000`.

## API Endpoints

- `GET /dashboard` - Fetches state-wise tourist data.
- `POST /login` - Authenticates user and returns JWT token.
- `POST /register` - Registers a new user and returns JWT token.
- `GET /map` - Provides map center coordinates and zoom level.

# 🚀 Developed with ❤️ by Yesu Balla
