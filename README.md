# Jobly API

Jobly is a **RESTful API** that serves as the backend for a job board application, allowing users to search for jobs, manage applications, and handle authentication securely using JWT tokens. This API follows best practices in authentication, authorization, and testing, ensuring a robust and developer-friendly experience.

---

## Features

- **Authentication & Authorization**: Secure login with JWT tokens.
- **User Roles**: Admin and regular user access control.
- **Job Listings**: Search, create, update, and delete job postings.
- **Company Management**: View company details and associated job postings.
- **User Profiles**: Manage user accounts and job applications.
- **Test Coverage**: Comprehensive unit and integration tests for models and routes.

---

## API Endpoints

### **Authentication**
- `POST /auth/token` - Login and receive a JWT token.
- `POST /auth/register` - Register a new user.

### **Users**
- `GET /users` - Get all users (Admin only).
- `GET /users/:username` - Get details of a specific user.
- `POST /users` - Create a new user (Admin only).
- `PATCH /users/:username` - Update a user (Admin or same user).
- `DELETE /users/:username` - Delete a user (Admin or same user).

### **Companies**
- `GET /companies` - Get a list of all companies (supports filtering).
- `GET /companies/:handle` - Get details of a specific company.
- `POST /companies` - Create a new company (Admin only).
- `PATCH /companies/:handle` - Update a company (Admin only).
- `DELETE /companies/:handle` - Delete a company (Admin only).

### **Jobs**
- `GET /jobs` - Get a list of all job postings (supports filtering).
- `GET /jobs/:id` - Get details of a specific job.
- `POST /jobs` - Create a new job (Admin only).
- `PATCH /jobs/:id` - Update a job (Admin only).
- `DELETE /jobs/:id` - Delete a job (Admin only).

### **Job Applications**
- `POST /users/:username/jobs/:id` - Apply for a job (Authenticated users).

---

## 🛠️ Technologies Used

- **Backend**: Express.js, Node.js
- **Database**: PostgreSQL
- **Authentication**: JWT (JSON Web Token)
- **Validation**: JSON Schema
- **Security**: Bcrypt, CORS
- **Logging**: Morgan

---

## 📦 Installation & Setup

### Prerequisites
Ensure you have **Node.js**, **PostgreSQL**, and **npm** installed.

### Steps
`git clone https://github.com/katiejnete/react-jobly-frontend.git`  
`cd react-jobly-frontend`  
`npm install`  
`npm start`   
