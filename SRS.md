# Software Requirements Specification (SRS)

## 1. Introduction
Smart Classroom is a mobile-friendly web application for attendance management, classroom interaction, and AI-assisted learning.

## 2. System Users
- **Student:** Registers attendance, submits feedback, answers polls, views lecture summaries, and receives AI homework reviews.
- **Lecturer:** Manages attendance, creates polls and assignments, reviews feedback, and generates AI lecture summaries and homework reviews.

## 3. Functional Requirements

### FR1 – Attendance Management
- Students register attendance using QR codes or session codes.
- Lecturers view attendance records and export CSV reports.
- The system prevents duplicate attendance registration.

### FR2 – People Counting
- Lecturers upload classroom photos.
- YOLOv8 detects and counts people without facial recognition.
- The system displays estimated classroom occupancy.

### FR3 – Student Feedback
- Students submit comments and suggestions.
- Lecturers view submitted feedback.

### FR4 – Live Polls
- Lecturers create multiple-choice polls.
- Students vote and lecturers view results.

### FR5 – AI Lecture Summaries
- Lecturers upload recordings or transcripts.
- AI generates summaries that lecturers can review and publish.
- Students view and download published summaries.

### FR6 – AI Homework Review
- Lecturers create assignments with deadlines.
- Students submit text or PDF solutions.
- AI analyzes submissions and provides detailed feedback.
- The system supports anonymous comparisons between submissions.

## 4. Non-Functional Requirements
- **Usability:** Simple and intuitive interface.
- **Compatibility:** Responsive on smartphones and computers.
- **Security:** Protect student data and restrict access by role.
- **Performance:** Provide reasonable response times.
- **Reliability:** Store attendance and submissions consistently.
- **Maintainability:** Use modular components.

## 5. System Constraints
- Follow the KISS principle.
- Reuse existing technologies and AI tools.
- No required integration with Moodle or university systems.

## 6. Prototype Scope
The functional prototype includes attendance management, YOLOv8 people counting, feedback, polls, AI lecture summaries, and AI homework reviews.

## 7. Acceptance Criteria
- Students can register attendance and lecturers can export attendance reports.
- YOLOv8 can detect and count people in uploaded classroom photos.
- Students can submit feedback and participate in polls.
- Lecturers can generate and publish AI lecture summaries.
- Students can view and download published summaries.
- Students and lecturers can request AI homework reviews.
- Homework comparisons use submissions from the same assignment.
- The application works on smartphones and computers.
