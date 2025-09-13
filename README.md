# LabAct-3-lab-auth-api

**Project Overview**

This project is a simple authentication API built with Node.js, Express, and MySQL. It implements JWT (JSON Web Tokens) for user authentication and includes features such as signup, login, logout, and profile access with token validation. The system also supports negative test cases such as invalid credentials, duplicate signup, and tampered/expired tokens.


**Features:**


**Authentication Operations**

POST /auth/signup – Register a new user

POST /auth/login – Authenticate user and issue JWT token

POST /auth/logout – Revoke a token and logout

GET /auth/profile – Access protected route (requires valid JWT)


**Error Handling**

Duplicate signup → 409 Conflict

Wrong password → 401 Unauthorized

Missing token on protected route → 401 Unauthorized

Tampered/expired token → 401 Unauthorized


**Database**

Connected to a MySQL database (lab_auth)

Includes users and revoked_tokens tables


**Server**

Node.js with Express

CORS enabled

Environment-based configuration with .env



**Project Structure**

lab-auth-api/

│── config/         # Database configuration

│── controllers/    # Authentication logic (signup, login, logout)

│── middleware/     # JWT auth middleware

│── routes/         # Authentication routes

│── server.js       # Main server file

│── package.json    # Dependencies and scripts

│── .env            # Environment variables



**Setup Instructions**

Prerequisites:

-Node.js
 (v22.x or compatible)
 
-XAMPP
 (for MySQL server)
 
-Postman
 (for API testing)
 
-Git



**1. Clone the repository:**

git clone https://github.com/smnrn/LabAct-3-lab-auth-api.git

cd LabAct-3-lab-auth-api



**2. Install dependencies:**

   npm install


   
**3. Configure the database connection by creating a .env file in the root directory:**

   DB_HOST=localhost
   
  DB_USER=root
  
  DB_PASSWORD=yourpassword
  
  DB_NAME=lab_auth
  
  PORT=5000
  
  JWT_SECRET=your_jwt_secret



**4. Run the server:**
   npm run dev

   * You should see: 🚀 Server running…  ✅ MySQL Connected


  
API Endpoints
**Health Check**

GET /health → API and database status



**Authentication**

POST /auth/signup → Register a new user

POST /auth/login → Login and receive a JWT token

POST /auth/logout → Logout and revoke token

GET /auth/profile → Access user profile (requires valid token)




**Learnings**

From this activity, I learned:

How to implement authentication using JWT in Node.js and MySQL

How to secure routes with middleware

How to structure a Node.js project with controllers, routes, and middleware

How to test APIs using Postman with both positive and negative test cases

How to use GitHub for version control and project documentation




