# Campus Course & Records Manager (CCRM)

## 📌 Project Overview
The **Campus Course & Records Manager (CCRM)** is a **console-based Java SE application** developed in BlueJ. It simulates a simple university records system, allowing administrators to manage students, courses, enrollments, grades, transcripts, and file operations (import/export/backup).

The project demonstrates **Object-Oriented Programming (OOP)**, advanced **Java SE features**, and several **design patterns**.

---

## 🎯 Features
### 1. Student Management
- Add, list, update, and deactivate students.
- Each student has:
    - `id`, `regNo`, `fullName`, `email`, `status`, `enrolledCourses`, `createdAt`.
- Print profile and transcript.

### 2. Course Management
- Add, list, update, and deactivate courses.
- Each course has:
    - `code`, `title`, `credits`, `instructor`, `semester`, `department`.
- Search and filter courses by **instructor, department, or semester** (using **Stream API**).

### 3. Enrollment & Grading
- Enroll/unenroll students (with business rules: max credits per semester).
- Record marks and compute letter grades & GPA.
- **Enums**:
    - `Semester { SPRING, SUMMER, FALL }`
    - `Grade { S, A, B, C, D, E, F }`
- Generate transcripts (using `toString()` overrides and polymorphism).

### 4. File Operations (NIO.2 + Streams)
- Import students/courses from CSV.
- Export current data to files.
- Backup data to a **timestamped folder**.
- Recursive utilities:
    - Compute total size of backup directory.
    - List files by depth.

### 5. CLI Workflow
- Menu-driven console app (runs in BlueJ terminal).
- Uses:
    - `if`, `switch`, `while`, `do-while`, `for`, `enhanced-for`.
    - Control statements (`break`, `continue`, `labeled break`).

---

## 🏗️ Technical Requirements Covered
- **OOP**:
    - Encapsulation: private fields + getters/setters.
    - Inheritance: `Person → Student, Instructor`.
    - Abstraction: `Person` abstract class with abstract methods.
    - Polymorphism: base-class references to subclasses.
- **Access Levels**: public, private, protected, default.
- **Immutability**: `CourseCode` class with `final` fields.
- **Nested Classes**: `Course.Builder` (static), `Transcript.LineItem` (inner).
- **Interfaces**: `Persistable`, `Searchable<T>`.
- **Functional Interfaces & Lambdas**: comparators, predicates.
- **Anonymous Inner Classes**: used in CLI callback.
- **Enums**: `Semester`, `Grade`.
- **Exceptions**:
    - Custom: `DuplicateEnrollmentException`, `MaxCreditLimitExceededException`.
    - Checked & unchecked, `try/catch/finally`.
- **Design Patterns**:
    - **Singleton**: `AppConfig`.
    - **Builder**: `Course.Builder`.
- **Java SE Features**:
    - NIO.2 (Path, Files).
    - Streams (filtering, aggregation).
    - Date/Time API (LocalDate, LocalDateTime).
    - Assertions.

---

## ⚙️ Project Setup

### 1. Prerequisites
- **Java JDK** (version 11 or 17 recommended).
- **BlueJ IDE** installed on your system.
- Basic knowledge of running console applications.

### 2. Clone or Download Project
- Clone from GitHub:
```bash
git clone https://github.com/SahaniJJ/CCRM_Java_VITyarthi.git
```
### 3. Open in BlueJ
1. Launch **BlueJ**.  
2. Go to **Project → Open Project…**  
3. Select the project folder (`CCRM/`).  
4. BlueJ will show class diagrams for all packages.  

---

### 4. Compile the Project
1. From the menu, select **Project → Compile All**.  
2. Ensure all classes are compiled successfully (boxes turn light blue).  

---

### 5. Run the Application
1. Right-click on `MainMenu` (inside the `edu.ccrm.cli` package).  
2. Choose **void main(String[] args)**.  
3. The BlueJ terminal will open and display the CLI menu.  
