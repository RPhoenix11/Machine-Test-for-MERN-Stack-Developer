# MERN Stack Application: Admin Dashboard with Agent Management and CSV Distribution

## **Overview**

This application is a MERN (MongoDB, Express.js, React.js, Node.js) stack-based solution designed to fulfill the following objectives:

1. **Admin User Login**: Secure authentication using JWT (JSON Web Tokens).
2. **Agent Creation & Management**: Add and manage agents with details like name, email, mobile number, and password.
3. **Uploading and Distributing Lists**: Upload CSV files containing lists of tasks, validate the file, and distribute the tasks equally among 5 agents.

---

## **Features**

### **1. User Login**
- Secure login with email and password.
- JWT-based authentication.
- Redirect to the dashboard on successful login.
- Error handling for invalid credentials.

### **2. Add Agents**
- Create agents with the following details:
  - Name
  - Email
  - Mobile Number (with country code)
  - Password
- Store agent details in MongoDB.

### **3. Upload CSV and Distribute Lists**
- Upload CSV files with the following columns:
  - `FirstName` (Text)
  - `Phone` (Number)
  - `Notes` (Text)
- Validate file format (accepts `.csv`, `.xlsx`, and `.xls`).
- Distribute tasks equally among 5 agents.
  - If the total number of tasks is not divisible by 5, distribute the remaining tasks sequentially.
- Save distributed lists in MongoDB.
- Display distributed lists for each agent on the frontend.

---

## **Technical Stack**

- **Frontend**: React.js / Next.js
- **Backend**: Express.js, Node.js
- **Database**: MongoDB
- **Authentication**: JSON Web Tokens (JWT)
- **File Upload**: CSV and Excel file handling

---

## **Setup and Installation**

### **Prerequisites**
- Node.js (v16 or higher)
- MongoDB (local or cloud-based)
- NPM or Yarn

### **Steps to Run the Application**

1. **Clone the Repository**
   ```bash
   git clone <repository-url>
   cd <project-folder>

2. **Install Dependencies**

Navigate to the backend folder and install dependencies:

  cd backend
  npm install

Navigate to the frontend folder and install dependencies:

cd ../frontend
npm install

3. **Set Up Environment Variables**

Create a .env file in the backend folder with the following variables:

env
MONGO_URI=<your-mongodb-connection-string>
JWT_SECRET=<your-jwt-secret-key>
PORT=5000

4. **Create a .env file in the frontend folder (if needed) for any frontend-specific configurations.**

Start the Backend Server

Navigate to the backend folder and run:

npm start
The backend server will start at http://localhost:5000.

5. **Start the Frontend Application**

Navigate to the frontend folder and run:

npm start
The frontend application will start at http://localhost:3000.

**FOLDER STRUCTURE**
mern-app/
├── backend/
│   ├── controllers/       # Backend controllers for handling requests
│   ├── models/            # MongoDB models (e.g., User, Agent, List)
│   ├── routes/            # API routes
│   ├── middleware/        # Middleware for authentication and validation
│   ├── utils/             # Utility functions (e.g., file upload, JWT)
│   ├── .env               # Environment variables
│   ├── server.js          # Entry point for the backend
├── frontend/
│   ├── public/            # Static assets
│   ├── src/
│   │   ├── components/    # React components
│   │   ├── pages/         # Application pages (e.g., Login, Dashboard)
│   │   ├── services/      # API service calls
│   │   ├── App.js         # Main application component
│   │   ├── index.js       # Entry point for the frontend
│   ├── .env               # Frontend environment variables
├── README.md              # Project documentation
