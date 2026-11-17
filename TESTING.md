# Testing Strategy – Smart Classroom

## 1. Testing Objective

The objective is to verify the functionality, reliability, and usability of the Smart Classroom application.

## 2. Unit Testing

Each software component will be tested independently.

| Class | Test | Expected Result |
|---|---|---|
| User | Invalid email | Access rejected |
| Student | Register attendance | Attendance updated |
| Lecturer | View attendance | Records displayed |
| Attendance | Duplicate registration | Duplicate prevented |
| PeopleCounter | Process classroom image | Estimated people count |
| Challenge | Submit location | Selection recorded |
| Feedback | Submit comment | Feedback saved |
| Poll | Submit answer | Answer recorded |
| AIService | Process lecture | Summary generated |
| ReportService | Export attendance | CSV file generated |

## 3. Integration Testing

- Verify communication between the frontend and backend.
- Verify attendance registration and database updates.
- Verify communication with YOLO.
- Verify feedback submission and lecturer dashboard updates.
- Verify attendance report generation.

## 4. System Testing

- Test the complete student attendance process.
- Test the lecturer dashboard.
- Test classroom people counting.
- Test feedback submission.
- Test classroom polls.

## 5. Usability Testing

- Test the application on smartphones and computers.
- Verify that navigation is simple and intuitive.
- Verify that buttons and messages are clear.
- Follow the KISS principle.

## 6. Initial Experimental Results

The initial Lovable prototype and YOLOv8 were tested separately.

| Test | Observed Result |
|---|---|
| Attendance registration | Successful in prototype |
| Attendance dashboard | Updated successfully |
| Student feedback | Submitted successfully |
| Mobile preview | Interface displayed |
| YOLO default configuration | 12 people detected |
| YOLO adjusted configuration | 25 people detected |

## 7. Limitations

- The current prototype uses sample data.
- Persistent database storage is not yet implemented.
- YOLO may miss people or produce false detections.
- Advanced AI services require further implementation and testing.

## 8. Conclusion

The initial experiments demonstrate the feasibility of the proposed solution. Additional testing is required for the complete system before real classroom deployment.
