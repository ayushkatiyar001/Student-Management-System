# Student Management System (SMS) 🎓

An enterprise-ready, modular console application engineered in Core Java to streamline student academic profiling, record tracking, and multi-metric grade calculations. This project serves as a comprehensive demonstration of core Object-Oriented Programming (OOP) architectures and data persistence structures.

---

## 📌 Project Overview

In educational institutions, managing student records and dynamically calculating grades based on varying evaluation metrics can be highly error-prone. This **Student Management System** provides an efficient, lightweight CLI environment to create, read, and process student entities while handling logical validations seamlessly.

---

## 🛠️ Core OOP Architecture & Principles Applied

This application translates foundational software engineering theories into practical, production-ready code modules:

### 1. Robust Inheritance Pattern (`super`)
- **Design:** Created a top-level abstract entity base class `Person` containing common biological attributes (`name`, `age`).
- **Implementation:** Extended `Person` into a specialized derived `Student` class. Used the `super()` and `super(name, age)` constructor chaining mechanisms to optimize object memory allocation and enforce rigid architectural reusability.

### 2. Polymorphism (Compile-time & Runtime)
- **Method Overloading:** Engineered two distinct logical signatures for `calculateGrade()`. 
  - One accepts a centralized `double marks` parameter for direct conversions.
  - The other acts as a multi-split business logic handler, accepting `int theoryMarks` and `int practicalMarks` to compute average evaluations.
- **Method Overriding:** Fully overrode the `displayInfo()` method utilizing the `@Override` annotation. By leveraging `super.displayInfo()`, the subclass dynamically injects derived entity states safely at runtime without mutating base behaviors.

### 3. Data Structuring & State Management
- Managed data states safely inside an **Array of Objects** (`Student[]`) bounded structurally within safe iterative indexing boundaries.
- Built explicit, input-sanitized interactive control flows using the `java.util.Scanner` interface, preventing structural memory leaks via explicit stream termination (`sc.close()`).

---
## 📊 Logical Flow Diagram

```text
[User Interface / Console Menu]
       │
       ├───► Choice 1: Add Student ───► Instantiates Student Object ───► Persists in Object Array
       │
       ├───► Choice 2: Display All ───► Loops Through Object Array ───► Triggers Polymorphic displayInfo()
       │
       ├───► Choice 3: Calculate ─────► Inputs Theory & Practical ─────► Evaluates Overloaded calculateGrade()
       │
       └───► Choice 4: Exit Process ──► Closes Scanner Input Stream ──► System Terminated Successfully
```
## 📋 Technical Prerequisites

- **Java Development Kit (JDK):** Version 8, 11, 17, or 21.
- **Environment Path:** Properly configured `JAVA_HOME` variables.
- **IDE Support:** IntelliJ IDEA (Recommended), Eclipse, or VS Code with Java Extension Pack.

---

## 💻 Installation & Local Deployment Steps

### Step 1: Clone the Repository
```bash
git clone [https://github.com/ayushkatiyar001/Student-Management-System.git](https://github.com/ayushkatiyar001/Student-Management-System.git)
cd Student-Management-System
