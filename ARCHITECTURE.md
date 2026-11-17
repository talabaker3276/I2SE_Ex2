# Software Architecture – Smart Classroom

## 1. Architecture Overview

Smart Classroom is designed using a modular client-server architecture. The system separates the user interface, application logic, data storage, and AI services.

## 2. Main Software Components

### 2.1 Frontend
- Provides student and lecturer interfaces.
- Supports smartphones and computers.
- Displays attendance, feedback, polls, and reports.

### 2.2 Backend
- Handles application requests.
- Validates student information.
- Manages attendance, feedback, and polls.
- Communicates with data storage and AI services.

### 2.3 Database
- Stores student information.
- Stores attendance records.
- Stores feedback, polls, and results.

### 2.4 People Counting Component
- Uses Python and YOLOv8.
- Processes classroom images.
- Detects and counts people.
- Returns the estimated number of people.

### 2.5 AI Services
- Generates lecture summaries.
- Analyzes homework submissions using LLMs.
- Provides feedback and comparisons.

### 2.6 Reporting Component
- Generates attendance reports.
- Supports CSV export for offline access.

## 3. Component Communication

1. Users interact with the frontend.
2. The frontend sends requests to the backend.
3. The backend processes requests and accesses the database.
4. AI components process images, lectures, and homework when required.
5. Results are returned to the user interface.

## 4. Prototype Implementation

The initial prototype was created using Lovable with local sample data. YOLOv8 was tested separately using Python.

The full backend, database, and advanced AI integrations are part of the proposed architecture and are not yet implemented.

## 5. Design Principles

- KISS – Keep It Simple.
- Modularity.
- Separation of concerns.
- Reusability.
- Maintainability.
- Data privacy.
