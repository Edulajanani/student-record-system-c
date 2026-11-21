# Student Record Management System (C Mini Project)

## Project Overview

The **Student Record Management System** is a menu-driven console application developed in C using **Singly Linked Lists, Dynamic Memory Allocation, Modular Programming, Searching, Sorting, and File Handling**.

This application allows users to manage student records containing Roll Number, Name, and Percentage. It supports adding, deleting, modifying, displaying, sorting, saving, and reversing student records.

Student records are maintained dynamically using a singly linked list and stored permanently in a file named `student.dat`.

## 🎯 Project Objective

To develop a modular and efficient Student Record Management System using C programming concepts.

The main objectives are:
- Understand singly linked list operations.
- Implement dynamic memory allocation using `malloc()` and `free()`.
- Perform searching, sorting, insertion, deletion, and modification.
- Implement file handling for storing and retrieving student records.
- Develop a menu-driven application using separate C modules.

## 📁 Project Module Structure

| File Name | Description |
|---|---|
| `addNewRec.c` | Adds a new student record with the smallest available positive roll number. |
| `delete.c` | Deletes student records using roll number or name. |
| `deleteall.c` | Deletes all student records and releases allocated memory. |
| `show.c` | Displays student records in a formatted tabular structure. |
| `mod.c` / `stud_mod.c` | Modifies student details using roll number, name, or percentage. |
| `sort.c` | Sorts student records alphabetically by name or by percentage in descending order. |
| `reverse.c` | Reverses the singly linked list by changing node links. |
| `save.c` | Saves student records into `student.dat` and loads records when the application starts. |
| `getroll.c` | Generates the smallest available positive roll number. |
| `search.c` | Supports searching student records. |
| `count.c` | Counts the total number of student records. |
| `main.c` / `driver_.c` | Contains the main menu and controls the overall program execution. |
| `header.h` | Contains structure definitions and function prototypes. |
| `makefile` | Automates compilation of all source modules (if available). |
| `student.dat` | Stores student records permanently. |

*Note: The module names can differ according to the implementation, provided all required responsibilities are covered.*

## 🧠 Student Record Structure

Each student record is maintained using the following structure:

```c
struct student
{
    int rollno;
    char name[50];
    float percentage;
    struct student *next;
};
```

- `rollno` – Stores the unique student roll number.
- `name` – Stores the student's name.
- `percentage` – Stores the student's percentage.
- `next` – Stores the address of the next node.

**Data Structure Used:** Singly Linked List.

## ✅ Features Implemented

### 1. Add New Record
- Creates a new node dynamically using `malloc()`.
- Automatically assigns the smallest available positive roll number.
- Accepts student name and percentage.
- Maintains unique roll numbers.

### 2. Delete Record
- Deletes records using roll number or name.
- Displays matching records when duplicate names exist.
- Allows the user to select the required record using its roll number.
- Releases deleted node memory using `free()`.

### 3. Display Records
- Displays all student records in a formatted table.
- Shows Roll Number, Name, and Percentage.
- Displays an appropriate message when no records are available.

### 4. Modify Record
Allows modification using:
- Roll Number
- Name
- Percentage

When multiple records match a name or percentage, the matching records are displayed and the user selects the required record using its roll number.

### 5. Save Records
- Saves all student records into `student.dat`.
- Restores previously saved records automatically when the application starts.
- Uses file handling for permanent data storage.

### 6. Sort Records
- Sorts student names in alphabetical order.
- Sorts student percentages in descending order (highest percentage first).

### 7. Delete All Records
- Deletes every node from the linked list.
- Releases allocated memory using `free()`.
- Sets the head pointer to `NULL`.
- Does not automatically delete or modify `student.dat`.

### 8. Reverse the List
- Reverses the entire singly linked list.
- Changes existing node links without creating additional nodes.

### 9. Exit Options

Provides two exit options:

- **S/s – Save and Exit:** Saves the current records, releases allocated memory, and terminates the program.
- **E/e – Exit Without Saving:** Discards unsaved changes, releases allocated memory, and terminates the program.

## 📋 Main Menu

```text
******** STUDENT RECORD MENU ********

a/A : Add new record
d/D : Delete a record
s/S : Show the list
m/M : Modify a record
v/V : Save records
e/E : Exit
t/T : Sort the list
l/L : Delete all the records
r/R : Reverse the list

Enter your choice:
```

The menu continues to appear until the user selects the Exit option.

## 🔍 Input Validation

The application handles the following input validations:

- Percentage must be between 0.00 and 100.00.
- Roll numbers must be positive and unique.
- Student names must not be empty.
- Invalid menu choices are handled appropriately.
- Attempts to delete or modify unavailable records are handled with suitable messages.

## 💾 File Handling System

The application uses a file named `student.dat` to store student records.

- **At startup:** Previously saved records are loaded from `student.dat`, if the file exists.
- **Save option:** Current records are written into `student.dat`.
- **Save and Exit:** Saves records before terminating.
- **Exit Without Saving:** Does not save the current changes.

## ⚙️ Compilation and Execution

**Using Makefile (if available):**

```bash
make
./student
```

**Manual GCC compilation:**

```bash
gcc *.c -o student
```

Run the application:

```bash
./student
```

The final executable name is `student`, as specified in the project assignment.

*Note: The manual compilation command assumes that all required C source modules are in the current directory and that there is only one `main()` function.*

## 🧠 Concepts Used

- C Programming
- Structures and Pointers
- Singly Linked Lists
- Dynamic Memory Allocation
- Functions and Modular Programming
- Searching and Sorting
- File Handling
- Memory Management

## 🎯 Purpose of This Project

- To understand the practical applications of linked lists.
- To improve C programming and problem-solving skills.
- To gain practical experience with dynamic memory allocation.
- To understand modular programming and file handling.
- To implement a simple database management application.

## 👩‍💻 Developer

**Edula Janani**

Student Record Management System

**Technologies:** C Programming | Singly Linked List | Dynamic Memory Allocation | File Handling
