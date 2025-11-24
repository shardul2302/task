# Invoice & User Management System - Quick Setup Guide

## 📋 Prerequisites
- Node.js (v14 or higher)
- MongoDB (cloud)
- npm 

## 📁 Project Structure
```
project-root/
├── backend-functional/     # Backend API
└── frontend/              # React Frontend
```

## 🚀 Quick Start

### 1. Backend Setup

```bash
# Navigate to backend folder
cd backend-functional

# Install dependencies
npm install

# Create .env file in backend-functional folder
# Add the following variables:
```

**`.env` file content:**
```env
PORT=5000
MONGODB_URI=mongodb://localhost:27017/invoice_db
```

```bash
# Start backend server
npm start
```
✅ Backend running on: `http://localhost:5000`

---

### 2. Frontend Setup

```bash
# Navigate to frontend folder
cd frontend

# Install dependencies
npm install

# Start frontend application
npm start
```
✅ Frontend running on: `http://localhost:3000`

---

## 🔑 Default Login Credentials

Create an admin user first or use existing credentials:
- Email: shardul@example.com
- Password: 123

---

## 📸 Application Overview

### Login Page
- User authentication with email/password
- Role-based access (ADMIN/USER)

### Invoice Dashboard
- View all invoices
- Search by invoice number or FY
- Filter by Financial Year
- Create, Edit, Delete invoices
- **Access**: All users

### User Dashboard
- Manage user accounts
- View user list with roles
- Create new users (USER role only)
- Edit user roles
- Delete users
- **Access**: ADMIN only

---

## ⚙️ Configuration

### Backend `.env` Variables
| Variable | Description | Example |
|----------|-------------|---------|
| `PORT` | Backend server port | `5000` |
| `MONGODB_URI` | MongoDB connection string | `mongodb://localhost:27017/invoice_db` |


### Frontend API Configuration
- Edit `src/config/api.js` if backend port changes
- Default: `http://localhost:5000`

---

## 🛠️ Troubleshooting

**Backend won't start?**
- Check if MongoDB is running
- Verify `.env` file exists and has correct values
- Ensure port 5000 is not in use

**Frontend won't connect?**
- Verify backend is running on port 5000
- Check API_BASE in `frontend/src/config/api.js`
- Clear browser cache and restart

**Login fails?**
- Check MongoDB connection
- Verify user exists in database
- Check backend console for errors

---

## 📦 Features

✅ User Authentication (Login/Logout)  
✅ Role-based Access Control (ADMIN/USER)  
✅ Invoice Management (CRUD operations)  
✅ User Management (ADMIN only)  
✅ Search & Filter functionality  
✅ Responsive UI  

---

## 🎯 Quick Commands

```bash
# Backend
cd backend-functional
npm install
npm start

# Frontend (in new terminal)
cd frontend
npm install
npm start
```

---

## 📝 Notes

- ADMIN users can access both Invoice and User dashboards
- USER role can only access Invoice dashboard
- Invoice Number and Financial Year combination must be unique
- Only USER accounts can be created from frontend (ADMIN via database)
