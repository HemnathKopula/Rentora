🚗 Rentora – Setup Instructions

Rentora is a full-stack car rental application built with React (Vite), Node.js/Express, and MongoDB, and deployed using Vercel.
🔧 Prerequisites

    Node.js (v18 or later)

    npm or yarn

    MongoDB URI (e.g., from MongoDB Atlas)

    Vercel CLI (optional, for local Vercel testing)

📁 1. Clone the Repository

git clone https://github.com/your-username/rentora.git
cd rentora

🌐 2. Frontend Setup (React + Vite)

cd client  # or your frontend directory
npm install

🔑 Create a .env file:

VITE_API_BASE_URL=https://your-backend-api.vercel.app/api

    Replace the URL with your deployed backend server URL.

To run locally:

npm run dev

🛠️ 3. Backend Setup (Express + MongoDB)

cd server  # or your backend directory
npm install

🔐 Create a .env file with the following:

PORT=5000
MONGO_URI=your_mongo_connection_string
JWT_SECRET=your_jwt_secret
CLIENT_URL=http://localhost:5173

    Update CLIENT_URL to the deployed frontend URL (e.g., https://rentora-ebon.vercel.app) when deploying.

To run locally:

npm run dev

🚀 4. Deployment Notes

    Frontend: Deploy on Vercel by importing the GitHub repo and setting environment variables in Vercel dashboard.

    Backend: Also deploy on Vercel (or alternatives like Render, Railway) and make sure CORS is configured like:

app.use(cors({
  origin: 'https://rentora-ebon.vercel.app',
  credentials: true,
}));

✅ Features

    JWT-based Authentication

    Car Listing & Booking

    Rental History

    Fully Responsive UI
