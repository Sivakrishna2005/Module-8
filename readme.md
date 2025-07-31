# 📚 Module 8 Assignment - Course Enrollment and Notifications

 

---

## 📝 Project Description

This module implements the Course Enrollment functionality for students and real-time WebSocket notifications for instructors in a Learning Management System (LMS). It features:

- Backend APIs for enrolling students and retrieving enrolled courses.
- Frontend UI for course listings and dynamic enrollments.
- Real-time instructor notifications when a new student enrolls using Socket.IO.

---

## 🚀 Features Implemented

### ✅ Backend
- POST /api/enroll: Enroll a student in a course (with validation).
- GET /api/enrollments/:userId: Fetch courses a student is enrolled in (with populated instructor details).
- Real-time WebSocket notification to instructors when a student enrolls.
- MongoDB + Mongoose integration for data handling.
- Validation for duplicate enrollments and course existence.

### ✅ Frontend
- CourseList.tsx to display all available courses to students.
- handleEnroll() function to enroll in a course using POST /enroll.
- Real-time notifications for instructors via Socket.IO client.
- Dynamic updates of course list and enrolled courses.

---

## 🛠 Tech Stack

- Frontend: React + TypeScript + Axios + Tailwind CSS
- Backend: Node.js + Express.js + Mongoose + TypeScript
- WebSockets: Socket.IO (server + client)
- Database: MongoDB (local or MongoDB Atlas)

---

## 📂 Folder Structure


Module8_Assignment_TarunAdithya/
│
├── backend/
│   ├── controllers/
│   │   └── enrollmentController.ts
│   ├── models/
│   │   └── Enrollment.ts
│   ├── routes/
│   │   └── enrollmentRoutes.ts
│   ├── server.ts (WebSocket server setup)
│   └── ...
│
├── frontend/
│   ├── components/
│   │   └── CourseList.tsx
│   ├── pages/
│   │   └── InstructorDashboard.tsx
│   ├── socket.ts (WebSocket client setup)
│   └── ...
│
└── README.md


---

## ⚙ Setup Instructions

### 1. Clone the Repository
 
git clone https://github.com/your-username/course-enrollment-system.git
cd course-enrollment-system




---

### 2. Setup Backend

 
cd backend
npm install


#### Create .env file:

PORT=5000
MONGO_URI=your_mongodb_connection_string


#### Start Backend Server:
 
npm run dev


---

### 3. Setup Frontend

 
cd ../frontend
npm install


#### Start Frontend App:
 
npm run dev


---

### 4. WebSocket Setup

- Backend: WebSocket server is configured in server.ts using Socket.IO.
- Frontend: socket.ts connects to WebSocket server and receives notifications.

---

## 🧪 Testing

### 📬 Enroll Student (POST)
Endpoint: /api/enroll

Payload:
json
{
  "studentId": "student123",
  "courseId": "course456"
}


### 📥 Get Enrolled Courses (GET)
Endpoint: /api/enrollments/student123

### 🧠 Real-Time Notification

- When a student enrolls, a socket event emits to the instructor client.
- Instructor Dashboard UI updates instantly with a new enrollment alert.

---

## 📸 Screenshots

> Include screenshots showing:
> - Course list page
> - Enrollment success
> - Instructor receiving real-time notification

---
