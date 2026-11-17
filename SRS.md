# Software Requirements Specification (SRS)

## 1. Introduction

Smart Classroom is a web-based teaching tool designed to improve classroom management, student participation, and communication between students and lecturers.

## 2. System Users

- **Student:** Registers attendance, submits feedback, answers polls, and receives homework reviews.
- **Lecturer:** Manages attendance, views feedback, creates polls, and receives lecture summaries.

## 3. Functional Requirements

### FR1 – Attendance Management
- Allow students to register attendance using their smartphones.
- Display present and absent students.
- Generate attendance reports in CSV format.
- Prevent duplicate attendance registration.

### FR2 – People Counting
- Allow classroom image upload.
- Use YOLO to detect and count people.
- Display the estimated number of people in the classroom.

### FR3 – Student Feedback
- Allow students to submit comments and suggestions.
- Allow lecturers to view submitted feedback.

### FR4 – Classroom Polls
- Allow lecturers to create polls.
- Allow students to submit answers.
- Display poll results.

### FR5 – Lecture Summaries
- Support AI-based summarization of recorded lectures.
- Present the main topics and key points.

### FR6 – Homework Review
- Support LLM-based homework analysis.
- Provide feedback and comparisons between submissions.

## 4. Non-Functional Requirements

- **Usability:** Simple and intuitive interface.
- **Compatibility:** Support smartphones and computers.
- **Performance:** Provide fast responses.
- **Security:** Protect student information.
- **Maintainability:** Use modular and understandable code.
- **Reliability:** Maintain consistent attendance records.

## 5. System Constraints

- Follow the KISS principle.
- Prefer existing software libraries and tools.
- No required integration with external university systems.

## 6. Prototype Scope

The prototype will prioritize attendance management and student feedback. YOLO will be evaluated separately for classroom occupancy estimation. Advanced AI features will be included in the system design.

## 7. Acceptance Criteria

- Students can register attendance successfully.
- Lecturers can view attendance records.
- Students can submit feedback.
- Lecturers can view submitted feedback.
- The interface is accessible on mobile devices.
