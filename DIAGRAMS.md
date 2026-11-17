# UML Diagrams – Smart Classroom

## 1. Class Diagram

```mermaid
classDiagram
    class User {
        +String email
        +String name
        +login()
    }

    class Student {
        +markAttendance()
        +submitFeedback()
        +answerPoll()
    }

    class Lecturer {
        +viewAttendance()
        +uploadImage()
        +createPoll()
        +openChallenge()
    }

    class Attendance {
        +String studentEmail
        +String lectureId
        +String status
        +register()
        +updateStatus()
    }

    class PeopleCounter {
        +detectPeople(image)
        +countPeople()
    }

    class Challenge {
        +String lectureId
        +String status
        +submitLocation()
        +resolveConflict()
    }

    class Feedback {
        +String comment
        +submit()
    }

    class Poll {
        +String question
        +List options
        +open()
        +close()
        +submitAnswer()
    }

    class AIService {
        +summarizeLecture()
        +reviewAssignments()
    }

    class ReportService {
        +exportCSV()
    }

    User <|-- Student
    User <|-- Lecturer
    Student --> Attendance
    Student --> Feedback
    Student --> Poll
    Student --> Challenge
    Lecturer --> Attendance
    Lecturer --> PeopleCounter
    Lecturer --> Challenge
    Lecturer --> Poll
    Lecturer --> AIService
    Lecturer --> ReportService
```

## 2. Sequence Diagram – Attendance Registration

```mermaid
sequenceDiagram
    actor Student
    participant WebApp
    participant Backend
    participant Database

    Student->>WebApp: Scan QR and enter email
    WebApp->>Backend: Register attendance
    Backend->>Database: Validate student
    Database-->>Backend: Student found
    Backend->>Database: Save attendance
    Backend-->>WebApp: Success
    WebApp-->>Student: Attendance confirmed
```

## 3. Sequence Diagram – People Counting and Challenge

```mermaid
sequenceDiagram
    actor Lecturer
    actor Student
    participant WebApp
    participant YOLO
    participant Database

    Lecturer->>WebApp: Upload classroom image
    WebApp->>YOLO: Detect people
    YOLO-->>WebApp: Count and bounding boxes
    WebApp->>Database: Get attendance count
    Database-->>WebApp: Registered count

    alt Counts match
        WebApp-->>Lecturer: Counts match
    else Counts differ
        WebApp-->>Lecturer: Mismatch detected
        Lecturer->>WebApp: Open challenge
        Student->>WebApp: Select location in image
        WebApp->>Database: Save selection
        Lecturer->>WebApp: Review and resolve conflicts
    end
```

## 4. Sequence Diagram – Student Feedback

```mermaid
sequenceDiagram
    actor Student
    participant WebApp
    participant Database
    actor Lecturer

    Student->>WebApp: Submit feedback
    WebApp->>Database: Save feedback
    WebApp-->>Student: Confirmation
    Lecturer->>WebApp: View feedback
    WebApp->>Database: Retrieve feedback
    Database-->>WebApp: Feedback list
    WebApp-->>Lecturer: Display feedback
```

## 5. Sequence Diagram – AI Analysis

```mermaid
sequenceDiagram
    actor Lecturer
    participant WebApp
    participant AIService

    Lecturer->>WebApp: Upload transcript or repository list
    WebApp->>AIService: Request analysis
    AIService-->>WebApp: Generated reports
    WebApp-->>Lecturer: Display results
```

## 6. Design Summary

The diagrams describe the proposed system architecture and interactions between the main software components. They represent the planned system rather than only the initial prototype.
