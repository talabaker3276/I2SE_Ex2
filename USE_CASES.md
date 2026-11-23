# Use Cases – Smart Classroom

## UC1 – Register Attendance
**Actor:** Student

1. The student logs into the web application.
2. The student scans a QR code or enters a session code.
3. The system validates and records attendance.
4. Duplicate registrations are prevented.

## UC2 – Manage Attendance
**Actor:** Lecturer

1. The lecturer creates an attendance session.
2. The system generates a QR code and session code.
3. The lecturer views attendance records.
4. Attendance data can be exported as CSV.

## UC3 – Count People
**Actor:** Lecturer

1. The lecturer uploads a classroom photo.
2. YOLOv8 detects and counts people.
3. The system displays the estimated count.
4. The lecturer compares the count with registered attendance.

## UC4 – Submit Feedback
**Actors:** Student and Lecturer

1. The student submits a comment or suggestion.
2. The system stores the feedback.
3. The lecturer views the feedback.

## UC5 – Live Poll
**Actors:** Lecturer and Student

1. The lecturer creates a multiple-choice poll.
2. Students submit their votes.
3. The lecturer views the results.

## UC6 – AI Lecture Summary
**Actors:** Lecturer and Student

1. The lecturer uploads a recording or transcript.
2. AI generates a structured lecture summary.
3. The lecturer reviews and publishes the summary.
4. Students view and download the published summary.

## UC7 – AI Homework Review
**Actors:** Lecturer and Student

1. The lecturer creates a homework assignment.
2. Students submit solutions as text or PDF.
3. Students and lecturers request detailed AI reviews.
4. AI identifies mistakes, strengths, and improvements.
5. The system supports anonymous comparisons between submissions from the same assignment.
