# Use Cases – Smart Classroom

## UC1 – Register Attendance

**Actor:** Student

**Main Flow:**
1. The student opens the web application.
2. The student enters their email address.
3. The student clicks Mark Attendance.
4. The system validates the student.
5. The system updates the attendance record.

**Alternative Flow:** If the email is invalid or attendance is already registered, the system displays a message.

## UC2 – View Attendance

**Actor:** Lecturer

**Main Flow:**
1. The lecturer opens the dashboard.
2. The system displays registered students.
3. The lecturer views attendance status.
4. The lecturer exports the attendance report as a CSV file.

## UC3 – Count People

**Actor:** Lecturer

**Main Flow:**
1. The lecturer uploads a classroom image.
2. YOLO processes the image.
3. The system detects people.
4. The system displays the estimated number of people.

## UC4 – Submit Feedback

**Actor:** Student

**Main Flow:**
1. The student opens the feedback section.
2. The student writes a comment or suggestion.
3. The student submits the feedback.
4. The lecturer can view the feedback.

## UC5 – Classroom Poll

**Actors:** Lecturer and Student

**Main Flow:**
1. The lecturer creates a poll.
2. Students submit their answers.
3. The system collects the answers.
4. The lecturer views the results.

## UC6 – Generate Lecture Summary

**Actor:** Lecturer

**Main Flow:**
1. The lecturer provides a recorded lecture.
2. The AI component processes the lecture content.
3. The system generates a summary.
4. The lecturer views the summary.

## UC7 – Homework Review

**Actors:** Student and Lecturer

**Main Flow:**
1. The student submits homework.
2. The LLM analyzes the submission.
3. The system generates feedback and comparisons.
4. The authorized users view the results.
