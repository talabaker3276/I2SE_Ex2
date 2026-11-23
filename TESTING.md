# Testing Strategy – Smart Classroom

## 1. Testing Objective
Verify the functionality, reliability, and usability of the Smart Classroom application through student and lecturer workflows.

## 2. Component Testing

| Component | Test | Expected Result |
|---|---|---|
| User | Login with valid account | Correct dashboard displayed |
| Attendance | Register attendance | Attendance saved |
| Attendance | Duplicate registration | Duplicate prevented |
| PeopleCounter | Upload classroom image | People detected and counted |
| Feedback | Submit comment | Comment visible to lecturer |
| Poll | Submit vote | Vote recorded |
| LectureSummary | Generate AI summary | Summary created |
| Assignment | Create homework | Assignment visible to students |
| Submission | Submit solution | Submission saved |
| AIService | Review homework | Detailed feedback generated |
| ReportService | Export attendance | CSV file generated |

## 3. Integration Testing
- Student attendance registration and lecturer dashboard updates.
- Classroom image processing using YOLOv8.
- Student feedback and live polls.
- AI lecture summary generation, publication, and download.
- Homework submission and AI review for students and lecturers.

## 4. Practical Test Results

| Test | Observed Result |
|---|---|
| Attendance registration | Successful |
| Lecturer attendance dashboard | Updated |
| Classroom people counting | Detected people in uploaded photos |
| Student polls | Voting worked |
| AI lecture summaries | Generated and published successfully |
| Student summary download | Successful |
| Homework submission | Successful |
| Student AI homework review | Generated detailed feedback |
| Lecturer AI homework review | Generated detailed feedback |
| Homework comparison | Requires testing with two submissions |
| Attendance CSV export | Requires file-content verification |

## 5. Usability Testing
- Tested student and lecturer interfaces.
- Verified mobile-friendly navigation.
- Followed the KISS principle.

## 6. Limitations
- YOLOv8 may miss people or generate false detections.
- Homework comparisons have not been tested with multiple submissions.
- Attendance CSV content requires further verification.
- AI-generated feedback may contain inaccuracies.

## 7. Conclusion
The functional prototype successfully demonstrated the main classroom workflows. Additional validation is recommended before real classroom deployment.
