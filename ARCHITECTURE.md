# Software Architecture – Smart Classroom

## 1. Architecture Overview
Smart Classroom uses a modular client-server architecture, separating the frontend, backend, database, and AI services.

## 2. Main Software Components

### 2.1 Frontend
- Responsive student and lecturer dashboards.
- Attendance, feedback, polls, lecture summaries, and homework interfaces.

### 2.2 Backend
- Handles user authentication and role-based access.
- Manages attendance, polls, feedback, and homework.
- Connects the database with AI services.

### 2.3 Database
- Stores users, attendance records, polls, and feedback.
- Stores homework submissions and AI-generated reviews.

### 2.4 People Counting
- Uses YOLOv8 to detect and count people in classroom photos.
- Displays estimated classroom occupancy without facial recognition.

### 2.5 AI Services
- Generates lecture summaries from recordings or transcripts.
- Analyzes homework and provides detailed feedback.
- Supports anonymous comparisons between submissions.

### 2.6 Reporting
- Displays attendance statistics.
- Exports attendance records as CSV files.

## 3. Component Communication
1. Users interact with the frontend.
2. The frontend sends requests to backend services.
3. The backend manages data and calls AI services when needed.
4. Results are displayed in the appropriate user dashboard.

## 4. Implementation
The functional prototype was built using Lovable and existing web technologies. Attendance, polls, feedback, AI lecture summaries, homework reviews, and YOLOv8 people counting are integrated into the application.

## 5. Design Principles
- KISS – Keep It Simple.
- Modularity and separation of concerns.
- Reusability and maintainability.
- Privacy and role-based access.
