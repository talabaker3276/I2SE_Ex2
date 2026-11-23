# Technical Tools Report – Smart Classroom

## 1. Objective
Evaluate existing technologies for developing a simple, mobile-friendly teaching application using the KISS principle.

## 2. Technologies

| Technology | Purpose | Status |
|---|---|---|
| Lovable | Web application development | Tested |
| Database & Authentication | User accounts and data storage | Functional workflows tested |
| YOLOv8 | Classroom people counting | Tested |
| QR Code | Attendance registration | Tested |
| AI Services | Lecture summaries and homework reviews | Tested |
| CSV | Attendance data export | Implemented; file verification pending |

## 3. Lovable Experiment

**Date:** 17/11/2026

A Smart Classroom prototype was developed using Lovable with student and lecturer dashboards.

**Results:**
- Attendance registration worked.
- Lecturer attendance records updated.
- Student feedback was submitted and displayed.
- The mobile interface was displayed successfully.
- Live polls were tested.
- AI lecture summaries were generated, published, and downloaded.
- Homework submissions received detailed AI reviews.

**Conclusion:** Lovable enabled rapid development of a functional web application.

## 4. YOLOv8 Experiment

YOLOv8n was tested using Python and Ultralytics on a classroom image (`p3.jpeg`).

| Parameter | Test 1 | Test 2 |
|---|---|---|
| Image size | 640 | 1280 |
| Confidence threshold | 0.25 | 0.15 |
| Detected persons | 12 | 25 |
| Inference time | 37.6 ms | 161.7 ms |

Increasing image resolution and reducing the confidence threshold increased detections. However, a false positive occurred when a person on a laptop screen was detected.

**Conclusion:** YOLOv8 is useful for estimating classroom occupancy but cannot independently verify student identities.

## 5. AI Experiments

- Generated a Hebrew lecture summary from recorded audio.
- Published the summary to the student dashboard.
- Successfully downloaded the published summary.
- Submitted a Python homework solution.
- AI identified a logical error involving negative numbers.
- Both student and lecturer received detailed AI feedback.

Anonymous homework comparison requires additional testing with multiple submissions.

## 6. Limitations

- YOLOv8 accuracy depends on image quality and visibility.
- AI-generated feedback may contain inaccuracies.
- Homework comparisons have not been tested with two submissions.
- Exported CSV content requires verification.
- The exact AI provider and backend configuration should be confirmed from the project settings.

## 7. Conclusion

The experiments demonstrate that existing web and AI technologies can support the Smart Classroom application. The main features were implemented and tested through practical user workflows.
