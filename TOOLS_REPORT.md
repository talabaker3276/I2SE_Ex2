# Technical Tools Report

## 1. Objective

The objective of this report is to evaluate existing technologies for building a simple, reliable, and mobile-friendly teaching tool.

The project follows the KISS principle and prioritizes software design over complex implementation.

## 2. Proposed Technologies

### Lovable
- Purpose: Building the web application and user interfaces.
- Advantage: Rapid development using AI-generated code.
- Test: Create a mobile-friendly prototype with student and lecturer interfaces.

### Supabase
- Purpose: Database management and email authentication.
- Advantage: Provides existing backend services.
- Test: Register a test user and store an attendance record.

### YOLO
- Purpose: Person detection and counting in classroom photos.
- Advantage: Counts people without identifying their personal identity.
- Test: Compare detected people with a manual count using classroom photos.
- Limitation: Detection accuracy may decrease due to distance, lighting, or occlusion.

### QR Code
- Purpose: Quick access to lecture attendance registration.
- Advantage: Simple interaction using a smartphone.
- Test: Generate and scan a QR code linked to a lecture.

### Gemini API
- Purpose: AI-based lecture analysis and assignment review.
- Advantage: Reuses an existing AI service.
- Test: Analyze a short lecture transcript and compare sample assignment repositories.
- Limitation: AI-generated reports may contain errors and require human review.

### CSV
- Purpose: Export attendance, feedback, and poll results.
- Advantage: Simple format compatible with Microsoft Excel and Google Sheets.
- Test: Export sample records and open the generated file.

## 3. Evaluation Criteria

- Ease of use
- Implementation complexity
- Reliability
- Mobile compatibility
- Privacy and security
- Cost

## 4. lovable

| Technology | Status |
|---|---|
| Lovable | Pending |
| Supabase | Pending |
| YOLO | Pending |
| QR Code | Pending |
| Gemini API | Pending |
| CSV | Pending |

Actual test results will be documented after testing each technology.

## 5. Preliminary Conclusion

The proposed technologies support a simple development approach based on existing tools and services.

Final technology selection will depend on practical testing results.

## 6. Practical Experiment – Lovable

Date: 17/11/2026

### Experiment Description

A simple Smart Classroom prototype was generated using Lovable with two interfaces: Student and Lecturer.

### Test Results

| Test | Result |
|---|---|
| Web application generation | PASS |
| Student interface | PASS |
| Lecturer interface | PASS |
| Attendance registration | PASS |
| Attendance counter | PASS |
| Feedback submission | PASS |
| Feedback display | PASS |
| Student mobile preview | PASS |

### Observations

- The student Omar was successfully marked as present.
- The attendance dashboard displayed 3 out of 5 students as present.
- A new feedback message was successfully submitted and displayed.
- The feedback counter increased from 2 to 3.
- The student interface displayed correctly in mobile preview.

### Limitations

- The prototype uses temporary sample data.
- No database or external API is connected.
- Data persistence and real authentication are not implemented.
- Testing on a physical mobile device is still pending.

### Conclusion

Lovable successfully generated a functional initial prototype and is suitable for further development of the teaching tool.
