PROJECT STUCTURE
🚀 Roadmap to Building the Platform Using Next.js
1️⃣ Project Planning & System Design

Before writing code, define the system structure.
Define the Main Users

3 MAIN ROLES:
*Admin
*Lecturer
\*Student

Define Core Modules
Module Description
Authentication - Login, signup, role management
Course Management - Lecturers create courses
Learning Materials - Upload slides, PDFs, videos
Exam Management - Create and schedule exams
AI Question Generation - Assist lecturers in generating questions
Online Examination - Students take exams
Anti-Cheating System - Prevent cheating
Result Management - Score calculation and result publishing

2️⃣ Tech Stack Architecture
Frontend
*Next.js
*TypeScript
*Tailwind CSS
*Shadcn UI

Backend
\*Using Next.js Server Actions / API Routes

Database
*PostgreSQL
*ORM
\*Prisma

Authentication
\*NextAuth.js

AI Integration
\*OpenAI API

Security
\*Browser monitoring

Webcam detection
\*Tab switching detection

3️⃣ System Folder Structure (Next.js)
app/
(auth)
login
register

(dashboard)
admin
lecturer
student

exams
courses
materials
results

components/
lib/
hooks/
database/

4️⃣ Phase 1: Authentication System

Features
*User Registration
*Login

Role-Based Access

Roles:
*Admin
*Lecturer
\*Student

Example flow:
Login → Detect Role → Redirect to dashboard

Dashboard routes:
/dashboard/admin
/dashboard/lecturer
/dashboard/student

5️⃣ Phase 2: Course & Learning Management

Lecturer Features
Lecturers should be able to:
*Create course
*Upload materials
\*Upload:
-PDF
-PPT
-Videos
-Notes

Example pages:
/courses
/courses/[id]
/courses/materials

Database example:
Course

- id
- title
- lecturerId
- semester

6️⃣ Phase 3: Question & Exam System

Lecturers can:
*Create exams
*Add questions
*Set timer
*Define exam date

Question Types
*Multiple choice
*True / False
\*Short answer

Example:
Exam

- id
- courseId
- duration
- startTime
- endTime

7️⃣ Phase 4: AI Question Generation

Using OpenAI API, lecturers can:

Input:
Topic: Data Structures
Difficulty: Medium
Questions: 10

AI generates:

*MCQ
*Answers
\*Explanations

Flow:
Lecturer → Enter topic → AI generates → Lecturer edits → Save

8️⃣ Phase 5: Online Examination System

Student flow:
Login
↓
View available exams
↓
Start exam
↓
Timer begins
↓
Submit answers

Key Features:
*Timer
*Auto submission
\*Question randomization

9️⃣ Phase 6: Anti-Cheating Mechanisms 🔐
Very important for your project defense.

Implement:
1️⃣ Tab Switching Detection
If student changes tab:
document.visibilitychange
System logs violation.

2️⃣ Fullscreen Mode
Force fullscreen during exam.

3️⃣ Disable Copy & Paste
Prevent:
Ctrl+C
Ctrl+V
Right click

4️⃣ Random Question Order
Each student receives different order.

5️⃣ Webcam Monitoring (Advanced)
Capture periodic screenshots.

6️⃣ Activity Log
Log:
*Tab switches
*Network issues
\*Exit attempts

🔟 Phase 7: Auto Marking System
Automatically grade:
*MCQ
*True/False

Manual grading:
\*Short answers by lecturer.

Result table example:
Result

- studentId
- examId
- score
- grade

1️⃣1️⃣ Phase 8: Result & Analytics
Students can see:
*Score
*Grade
\*Feedback

Lecturers can see:
*Class performance
*Highest score
*Lowest score
*Average score

Charts using:
\*Chart.js

1️⃣2️⃣ Phase 9: Admin System
Admin manages:
*Users
*Courses
*System logs
*Reports

Admin dashboard:
Total students
Total exams
Exam activity logs

1️⃣3️⃣ Phase 10: Security & Performance
Add:
*Rate limiting
*JWT protection
*Input validation
*Encrypted passwords

Use:
\*bcrypt

1️⃣4️⃣ Phase 11: Deployment
Deploy using:
*Vercel
Database hosting:
*Supabase

🧠 Architecture Overview
Next.js (Frontend + Backend)
↓
API Routes
↓
Prisma ORM
↓
PostgreSQL Database
↓
AI Integration (OpenAI)

🎯 Minimum Viable Product (Important for Final Year)
You DO NOT need everything.
Minimum version:
✅ Authentication
✅ Course materials upload
✅ Exam creation
✅ Online exam interface
✅ Auto marking
✅ Results page
✅ Basic anti-cheating

⭐ Features That Will Impress Your Supervisors
Add 2–3 advanced features:
*AI Question Generator
*Tab switch detection
*Question randomization
*Exam analytics dashboard
