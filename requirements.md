# Airbnb Clone Backend – Requirement Specifications

This document outlines the technical and functional requirements for three major backend features of the Airbnb Clone project.

---

## 1. 🧾 User Authentication

### ✅ Functional Requirements:
- Allow users to **register**, **log in**, and **log out**
- Support for **role-based access** (User, Host, Admin)
- Secure password handling with hashing (e.g., bcrypt)
- Email format validation and uniqueness checks

### 🌐 API Endpoints:
| Method | Endpoint          | Description         |
|--------|-------------------|---------------------|
| POST   | /api/register     | Create user account |
| POST   | /api/login        | Authenticate user   |
| POST   | /api/logout       | End user session    |

### 📥 Input Specifications:
- `username`: string, required, unique
- `email`: string, required, valid email format
- `password`: string, required, min 8 characters

### 📤 Output Example:
```json
{
  "message": "User registered successfully",
  "user": {
    "id": 1,
    "username": "allen",
    "email": "allen@example.com",
    "role": "User"
  }
}
