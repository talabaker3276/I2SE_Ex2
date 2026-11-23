# UML Diagrams – Smart Classroom

## 1. Class Diagram

```mermaid
classDiagram
    User <|-- Student
    User <|-- Lecturer

    class User {
        +String email
        +String name
        +login()
    }

    class Student {
        +markAttendance()
        +submitFeedback()
        +answerPoll()
        +submitHomework()
        +requestAIReview()
    }

    class Lecturer {
        +createSession()
        +viewAttendance()
        +createPoll()
        +createAssignment()
        +publishSummary()
    }

    class Attendance {
        +String studentId
        +String sessionId
        +String status
        +register()
    }

    class PeopleCounter {
        +detectPeople(image)
        +countPeople()
    }

    class Feedback {
        +String comment
        +submit()
    }

    class Poll {
        +String question
        +List options
        +submitVote()
    }

    class LectureSummary {
        +String content
        +String status
        +publish()
        +download()
    }

    class Assignment {
        +String title
        +Date deadline
        +create()
    }

    class Submission {
        +String content
        +submit()
    }

    class AIService {
        +summarizeLecture()
        +reviewHomework()
        +compareSubmissions()
    }

    class ReportService {
        +exportCSV()
    }

    Student --> Attendance
    Student --> Feedback
    Student --> Poll
    Student --> Submission
    Lecturer --> Attendance
    Lecturer --> PeopleCounter
    Lecturer --> Poll
    Lecturer --> Assignment
    Lecturer --> LectureSummary
    Lecturer --> ReportService
    Assignment --> Submission
    AIService --> LectureSummary
    AIService --> Submission
```

## 2. Sequence Diagram – Attendance

```mermaid
sequenceDiagram
    actor Student
    participant WebApp
    participant Backend
    participant Database

    Student->>WebApp: Scan QR or enter session code
    WebApp->>Backend: Register attendance
    Backend->>Database: Validate student and session
    Database-->>Backend: Validation result
    Backend->>Database: Save attendance
    Backend-->>WebApp: Confirmation
    WebApp-->>Student: Attendance registered
```

## 3. Sequence Diagram – AI Lecture Summary

```mermaid
sequenceDiagram
    actor Lecturer
    actor Student
    participant WebApp
    participant AIService
    participant Database

    Lecturer->>WebApp: Upload recording or transcript
    WebApp->>AIService: Generate summary
    AIService-->>WebApp: Structured summary
    WebApp-->>Lecturer: Display draft
    Lecturer->>WebApp: Publish summary
    WebApp->>Database: Save published summary
    Student->>WebApp: View summaries
    WebApp->>Database: Retrieve published summaries
    Database-->>WebApp: Summary
    WebApp-->>Student: Display and download
```

## 4. Sequence Diagram – AI Homework Review

```mermaid
sequenceDiagram
    actor Student
    actor Lecturer
    participant WebApp
    participant Database
    participant AIService

    Lecturer->>WebApp: Create assignment
    WebApp->>Database: Save assignment
    Student->>WebApp: Submit text or PDF
    WebApp->>Database: Save submission
    Student->>WebApp: Request AI review
    WebApp->>AIService: Analyze submission
    AIService-->>WebApp: Detailed feedback
    WebApp-->>Student: Display AI review
    Lecturer->>WebApp: Request homework review
    WebApp->>AIService: Analyze submission
    AIService-->>WebApp: Detailed feedback
    WebApp-->>Lecturer: Display AI review
```

## 5. Design Summary

These diagrams describe the main components and interactions of the Smart Classroom prototype. They are simplified design models rather than an exact representation of the generated source code.
