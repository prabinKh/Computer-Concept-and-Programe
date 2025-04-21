Unit 2: Overview of C Language
This repository provides an educational resource for Unit 2: Overview of C Language, covering the fundamentals of C programming. It includes a practical C program (student_grade_calculator.c) that calculates a student’s average grade and determines their letter grade, serving as a real-world example. Additional example code snippets (e.g., payroll calculator, temperature converter) are provided for each topic to illustrate concepts like character set, tokens, and debugging. The README explains each topic with detailed explanations, practical examples, and references to the provided arithmetic_operations.c for continuity.
This resource is designed for students and beginners learning C programming.
Table of Contents

Introduction to C
C Character Set
Tokens
Identifiers
Keywords
Constants
Variables
Data Types
Type Conversion
Operators and Expressions
Structure of a C Program
Managing Input and Output Operations
Common Errors in Programming
Debugging Basics
How to Run the Program
Contributing
License

1. Introduction to C
Explanation
C is a general-purpose, procedural programming language developed by Dennis Ritchie in 1972. It is efficient, flexible, and widely used for system programming, embedded systems, and applications. C is the foundation for languages like C++ and Java.
Key Features

Structured programming.
Fast execution.
Memory access via pointers.
Portable.

Practical Example: Student Grade Calculator
student_grade_calculator.c takes marks for three subjects, computes the average, and assigns a letter grade (A, B, C, D, F).
#include <stdio.h>
int main() {
    float mark1, mark2, mark3, average;
    char grade;
    printf("Enter marks for Subject 1 (out of 100): ");
    scanf("%f", &mark1);
    printf("Enter marks for Subject 2 (out of 100): ");
    scanf("%f", &mark2);
    printf("Enter marks for Subject 3 (out of 100): ");
    scanf("%f", &mark3);
    average = (mark1 + mark2 + mark3) / 3;
    if (average >= 90) grade = 'A';
    else if (average >= 80) grade = 'B';
    else if (average >= 70) grade = 'C';
    else if (average >= 60) grade = 'D';
    else grade = 'F';
    printf("Average: %.2f\nGrade: %c\n", average, grade);
    return 0;
}

Additional Example
A library system welcome message:
#include <stdio.h>
int main() {
    printf("Welcome to the Library Management System!\n");
    printf("1. Borrow Book\n2. Return Book\n");
    return 0;
}

Real-Life Context: Used in educational software and library kiosks.
2. C Character Set
Explanation
The C character set includes letters (A-Z, a-z), digits (0-9), special characters (e.g., +, @), and whitespace (space, tab, newline).
Example (From student_grade_calculator.c)
Uses letters (m, a, r, k), digits (90), and special characters (/ in average = ... / 3).
Additional Example
Password character validator:
#include <stdio.h>
int main() {
    char letter = 'A';
    char digit = '5';
    char special = '@';
    printf("Valid password characters:\nLetter: %c\nDigit: %c\nSpecial: %c\n", letter, digit, special);
    return 0;
}

Real-Life Context: Password validation in login systems.
3. Tokens
Explanation
Tokens are the smallest units in C: keywords, identifiers, constants, operators, and symbols.
Example (From student_grade_calculator.c)
float average = (mark1 + mark2 + mark3) / 3; includes:

Keywords: float
Identifiers: average, mark1, mark2, mark3
Constants: 3
Operators: =, +, /

Additional Example
Rectangle area calculator:
#include <stdio.h>
int main() {
    int length = 10;
    int width = 5;
    int area = length * width;
    printf("Area: %d\n", area);
    return 0;
}

Real-Life Context: Architectural software for area calculations.
4. Identifiers
Explanation
Identifiers are user-defined names for variables/functions. Rules: start with a letter/underscore, include letters/digits/underscores, case-sensitive.
Example (From student_grade_calculator.c)
Identifiers: mark1, mark2, mark3, average, grade.
Additional Example
Employee details:
#include <stdio.h>
int main() {
    int employee_id = 101;
    float employee_salary = 45000.50;
    char employee_grade = 'B';
    printf("Employee ID: %d\nSalary: %.2f\nGrade: %c\n", employee_id, employee_salary, employee_grade);
    return 0;
}

Real-Life Context: HR systems for employee records.
5. Keywords
Explanation
Keywords are reserved words (e.g., int, if, return) with predefined meanings.
Example (From student_grade_calculator.c)
Keywords: int, float, char, if, else, return.
Additional Example
Number classifier:
#include <stdio.h>
int main() {
    int number;
    printf("Enter a number: ");
    scanf("%d", &number);
    if (number > 0) printf("Positive\n");
    else printf("Non-positive\n");
    return 0;
}

Real-Life Context: Financial systems checking balances.
6. Constants
Explanation
Constants are fixed values: integers (10), floating-point (3.14), characters ('A'), strings ("Hello").
Example (From student_grade_calculator.c)
Constants: 3, 90, 'A', "Average: %.2f\n".
Additional Example
Circle area:
#include <stdio.h>
const float PI = 3.14159;
int main() {
    float radius = 7.0;
    float area = PI * radius * radius;
    printf("Circle Area: %.2f\n", area);
    return 0;
}

Real-Life Context: Engineering software for geometric calculations.
7. Variables
Explanation
Variables are named memory locations that store changeable data.
Example (From student_grade_calculator.c)
Variables: mark1, mark2, mark3, average, grade.
Additional Example
Inventory tracker:
#include <stdio.h>
int main() {
    int stock_quantity = 100;
    int items_sold = 25;
    stock_quantity = stock_quantity - items_sold;
    printf("Remaining Stock: %d\n", stock_quantity);
    return 0;
}

Real-Life Context: Inventory management systems.
8. Data Types
Explanation
Data types define variable storage: int, float, double, char, etc.
Example (From student_grade_calculator.c)
float for marks, char for grade, int for main.
Additional Example
Product details:
#include <stdio.h>
int main() {
    int product_id = 5001;
    float product_price = 29.99;
    char product_category = 'E';
    double discount_rate = 0.15;
    printf("Product ID: %d\nPrice: %.2f\nCategory: %c\nDiscount: %.2f\n", 
           product_id, product_price, product_category, discount_rate);
    return 0;
}

Real-Life Context: E-commerce product listings.
9. Type Conversion
Explanation
Type conversion changes data types: implicit (automatic) or explicit (casting).
Example (From student_grade_calculator.c)
average = (mark1 + mark2 + mark3) / 3; (implicit int to float).
Additional Example
Temperature converter:
#include <stdio.h>
int main() {
    int celsius = 25;
    float fahrenheit = (float)(celsius * 9 / 5) + 32;
    printf("Temperature: %.2f°F\n", fahrenheit);
    return 0;
}

Real-Life Context: Weather apps.
10. Operators and Expressions
Explanation
Operators perform operations; expressions combine operands and operators.
Example (From student_grade_calculator.c)
average = (mark1 + mark2 + mark3) / 3; uses +, /, =.
Additional Example
Net pay calculator:
#include <stdio.h>
int main() {
    float gross_pay = 5000.0;
    float tax_rate = 0.2;
    float tax = gross_pay * tax_rate;
    float net_pay = gross_pay - tax;
    printf("Gross Pay: %.2f\nTax: %.2f\nNet Pay: %.2f\n", gross_pay, tax, net_pay);
    return 0;
}

Real-Life Context: Payroll systems.
11. Structure of a C Program
Explanation
Structure: preprocessor directives, main function, declarations, statements, return.
Example (From student_grade_calculator.c)
Includes #include, main, variable declarations, and return 0.
Additional Example
Countdown timer:
#include <stdio.h>
int main() {
    int seconds = 5;
    while (seconds > 0) {
        printf("Time left: %d seconds\n", seconds);
        seconds--;
    }
    printf("Time's up!\n");
    return 0;
}

Real-Life Context: Quiz apps or timers.
12. Managing Input and Output Operations
Explanation
scanf for input, printf for output, with format specifiers.
Example (From student_grade_calculator.c)
scanf("%f", &mark1);, printf("Average: %.2f\n", average);.
Additional Example
User feedback:
#include <stdio.h>
int main() {
    char feedback[50];
    int rating;
    printf("Enter your feedback: ");
    scanf("%s", feedback);
    printf("Enter rating (1-5): ");
    scanf("%d", &rating);
    printf("Feedback: %s\nRating: %d/5\n", feedback, rating);
    return 0;
}

Real-Life Context: Customer feedback systems.
13. Common Errors in Programming
Explanation
Errors: syntax (e.g., missing ;), logical (e.g., wrong logic), runtime (e.g., division by zero).
Example (From student_grade_calculator.c)
Logical error: Wrong threshold (average >= 90 vs. >= 85).
Additional Example
Error-prone code:
#include <stdio.h>
int main() {
    int x = 10;
    int y = 0;
    if (y != 0) printf("Result: %d\n", x / y); // Avoids runtime error
    else printf("Error: Division by zero\n");
    printf("Done\n"); // Fixed syntax error
    return 0;
}

Real-Life Context: Banking software error handling.
14. Debugging Basics
Explanation
Debugging uses print statements, compilers, IDEs, and testing.
Example (From student_grade_calculator.c)
printf("Debug: mark1 = %.2f\n", mark1); to verify input.
Additional Example
Square calculator:
#include <stdio.h>
int main() {
    int num;
    printf("Enter a number: ");
    scanf("%d", &num);
    printf("Debug: Input num = %d\n", num);
    int square = num * num;
    printf("Debug: Square = %d\n", square);
    printf("Square of %d is %d\n", num, square);
    return 0;
}

Real-Life Context: Robotics sensor calculations.
How to Run the Program

Prerequisites: Install gcc (e.g., brew install gcc on macOS).
Steps:
Clone: git clone <repository-url>
Compile: gcc student_grade_calculator.c -o student_grade_calculator
Run: ./student_grade_calculator
Test examples by creating .c files and compiling similarly.



Contributing
Add examples, improve student_grade_calculator.c, or enhance the README. Fork, branch, commit, push, and open a pull request.
License
MIT License. See LICENSE file.
Contact
Open an issue on GitHub for questions.
