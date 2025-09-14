⭐ Store Rating App

A full-stack web application for rating and reviewing stores.
Users can register, log in, browse stores, submit ratings/reviews, and view dashboards.
The system also supports admin and store owner dashboards for management.

🚀 Features

🔐 User authentication (JWT-based login/register)

🏪 Add, update, delete stores (store owner)

⭐ Submit and view store ratings/reviews

📊 Average rating calculation with star display

👨‍💻 Admin dashboard for managing users and stores

🎨 React-based UI with reusable components

🛠️ Tech Stack

Frontend: React (Vite), JSX, Axios
Backend: Node.js, Express, SQL Database
Database: SQL (schema included in backend/config/database.sql)
Auth: JWT, Bcrypt
Other Tools: dotenv, Nodemon

📂 Project Structure
store_rating_app/
│
├── backend/
│   ├── config/
│   │   └── database.sql        # SQL schema for users, stores, ratings
│   ├── middleware/
│   │   ├── auth.js             # JWT auth middleware
│   │   └── validation.js       # Input validation
│   ├── models/
│   │   ├── User.js             # User model
│   │   ├── Store.js            # Store model
│   │   └── Rating.js           # Rating model
│   ├── routes/
│   │   ├── auth.js             # Login/Register APIs
│   │   ├── users.js            # User management APIs
│   │   ├── stores.js           # Store CRUD APIs
│   │   └── ratings.js          # Ratings APIs
│   ├── .env                    # Environment variables
│   ├── server.js               # Backend entry point
│   └── package.json            # Backend dependencies
│
├── frontend/
│   ├── public/
│   │   ├── components/
│   │   │   ├── Navbar.jsx      # Navigation bar
│   │   │   ├── StoreCard.jsx   # Store display card
│   │   │   └── RatingStars.jsx # Star rating UI
│   │   ├── pages/
│   │   │   ├── Login.jsx       # Login page
│   │   │   ├── Register.jsx    # Register page
│   │   │   ├── Dashboard.jsx   # User dashboard
│   │   │   ├── Stores.jsx      # List of stores
│   │   │   ├── AdminDashboard.jsx      # Admin panel
│   │   │   └── StoreOwnerDashboard.jsx # Store owner panel
│   └── package.json            # Frontend dependencies
│
└── README.md

⚙️ Installation & Setup
1. Clone the repository
git clone https://github.com/your-username/store-rating-app.git
cd store-rating-app

2. Backend Setup
cd backend
npm install


Create .env in backend/ with:

PORT=5000
DB_HOST=localhost
DB_USER=your_db_user
DB_PASSWORD=your_db_password
DB_NAME=store_rating_db
JWT_SECRET=your_jwt_secret


Import database schema:

mysql -u your_db_user -p store_rating_db < config/database.sql


Run backend:

npm run dev

3. Frontend Setup
cd ../frontend
npm install
npm run dev


Frontend will run on: http://localhost:5173
Backend will run on: http://localhost:5000

📌 API Routes
Auth

POST /api/auth/register → Register user

POST /api/auth/login → Login

Users

GET /api/users → Get all users (admin only)

Stores

GET /api/stores → Get all stores

POST /api/stores → Add new store (store owner)

PUT /api/stores/:id → Update store

DELETE /api/stores/:id → Delete store

Ratings

POST /api/ratings/:storeId → Add rating

GET /api/ratings/:storeId → Get ratings for a store

🖼️ Screenshots

(Add your screenshots here once UI is ready!)

🤝 Contribution

Fork this repository

Create a new branch (feature-xyz)

Commit your changes

Open a Pull Request
