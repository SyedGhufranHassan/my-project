# 📚 Student Gradebook (Go CLI Application)

A simple command-line application written in Go for managing student records and grades. Users can add students with their grades, calculate average grades, list all students, and delete student records interactively.

## 🚀 Features

- ✅ Add a student and their grades  
- 📊 Calculate and view a student's average grade  
- 📋 List all students with their grades  
- ❌ Delete a student record  
- 🛑 Exit the application gracefully  

## 🗂️ Project Structure

```
student-gradebook/
├── go.mod                 # Go module definition
├── main.go                # Main application logic & CLI interface
├── README.md
├── reader.go              # Utility to read user input from console
├── student/               # Handles student data and grade operations
│   ├── student.go         # Core functions to manage the gradebook
│   └── student_types.go   # Student struct definition (future extensibility)
└── utils/
    └── parse.go           # Utility function to parse input grades

```

## 📦 Installation

1. **Clone the Repository**
   ```bash
   git clone https://github.com/yourusername/student-gradebook.git
   cd student-gradebook
   ```

2. **Run the Application**
   ```bash
   go run .
   ```

## 💻 How to Use

When you run the app, you'll see a menu like this:

```
--- Student Gradebook ---
1. Add Student
2. Get Average
3. List All Students
4. Delete Student
5. Exit
Enter your choice:
```

### ✅ 1. Add Student
- Input a name.
- Provide grades separated by commas (e.g., `90, 85, 78`).

### 📊 2. Get Average
- Enter the name of the student to see their average grade.

### 📋 3. List All Students
- Displays all student names and their grades.

### ❌ 4. Delete Student
- Enter the student name to remove them from the system.

### 🛑 5. Exit
- Exits the application.

## 🧠 Example Usage

```
--- Student Gradebook ---
1. Add Student
2. Get Average
3. List All Students
4. Delete Student
5. Exit
Enter your choice: 1
Enter student name: Alice
Enter grades (comma-separated): 88, 92, 79
Student added successfully!

Enter your choice: 2
Enter student name: Alice
Average grade for Alice: 86.33
```

## 🛠️ Tech Stack

- **Language**: Go  
- **Standard Packages**: `fmt`, `os`, `bufio`, `strings`, `strconv`

## 📌 Notes

- This project uses an in-memory map to store data. All student records will be lost once the program exits.
- Designed for simplicity and extensibility.

