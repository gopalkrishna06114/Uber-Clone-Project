# 🚖 Uber Clone (MERN Stack)

This is a **full-stack Uber Clone** built using the **MERN stack (MongoDB, Express.js, React, Node.js)**.  
It implements **user and driver authentication**, **Google Maps API integration** for real-time location, and allows users to **create rides** while drivers can **accept rides** with three different vehicle types (**Car, Bike, Auto**).  

⚠️ **Note**: This project is designed **only for mobile screens** and is not optimized for laptop or desktop screens.

---

## 📌 Features

- 🔑 **Authentication**  
  - User signup/login  
  - Driver signup/login  
  - JWT token-based authentication  
  - MongoDB used for authentication database  

- 📍 **Google Maps Integration**  
  - Users can share their exact location  
  - Live ride tracking  
  - Drivers see ride requests in real-time  

- 🚘 **Ride Functionality**  
  - User can book a ride  
  - Driver can accept/reject rides  
  - Multiple vehicle types available:  
    - Car  
    - Bike  
    - Auto  

- ⚡ **Tech Stack**  
  - **Frontend**: React (Vite), Tailwind CSS, Google Maps API, Socket.io-client  
  - **Backend**: Node.js, Express.js, Socket.io  
  - **Database**: MongoDB  
  - **Other Tools**: Axios, ESLint, GSAP animations  

---

## 📂 Project Structure

```
uber-clone/
│
├── frontend/              # React + Vite frontend
│   ├── public/            # Static files
│   ├── src/               # React components, routes, and logic
│   ├── package.json       # Frontend dependencies
│   └── vite.config.js     # Vite configuration
│
├── backend/               # Node.js + Express backend
│   ├── models/            # MongoDB models (User, Driver, Ride)
│   ├── routes/            # Authentication & ride APIs
│   ├── controllers/       # Business logic
│   ├── server.js          # Entry point of backend
│   └── package.json       # Backend dependencies
│
├── .env                   # Environment variables (API keys, DB URI)
├── .gitignore             # Ignored files for Git
└── README.md              # Documentation
```

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the Repository
```
git clone https://github.com/your-username/uber-clone.git
cd uber-clone
```

### 2️⃣ Setup Environment Variables
Create a `.env` file in **both frontend and backend** directories.

Example `.env` values:
```
VITE_BASE_URL=http://localhost:4000
GOOGLE_MAPS_API=your-google-maps-api-key
MONGO_URI=your-mongodb-uri
JWT_SECRET=your-secret-key
PORT=4000
```

### 3️⃣ Install Dependencies
Frontend:
```
cd frontend
npm install
```

Backend:
```
cd ../backend
npm install
```

### 4️⃣ Run the Project
Start backend:
```
cd backend
npm start
```

Start frontend:
```
cd ../frontend
npm run dev
```

### 5️⃣ Access the App
- Open **http://localhost:5173** in mobile view (or use browser dev tools → mobile mode).  
- **Users** can sign up, log in, and request rides.  
- **Drivers** can log in, view ride requests, and accept them.  

---

## 📱 Notes
- This project is **mobile-only** (not compatible with laptop/desktop screens).  
- Enable Google Maps API from your **Google Cloud Console**.  
- Use **MongoDB Atlas** or local MongoDB for database connection.  

---

## 🤝 Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you’d like to change.

---

## 📜 License
This project is for **educational purposes only** and is **not affiliated with Uber**.  
