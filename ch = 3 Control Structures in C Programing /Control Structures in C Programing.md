# Unit 3: Control Structures in C Programming

This repository is an educational resource for **Unit 3: Control Structures in C Programming**, covering essential constructs for controlling program flow in C. The topics include **Introduction to Control Structures**, **Decision Making Statements**, **Looping Statements**, **Branching Statements**, and **Common Pitfalls** (e.g., infinite loops, misplacement of conditionals). Each topic is briefly explained, accompanied by multiple example C programs (more than 20 in total) and real-world scenarios to illustrate practical applications. The repository also includes references to the `arithmetic_operations.c` program (which performs arithmetic operations on two user-input numbers) and concludes with over 20 exam-style questions and solutions relevant to these topics.

This resource is designed for students and beginners learning C programming as part of a computer science curriculum.

## Table of Contents

- [Introduction to Control Structures](#1-introduction-to-control-structures)
- [Decision Making Statements](#2-decision-making-statements)
- [Looping Statements](#3-looping-statements)
- [Branching Statements](#4-branching-statements)
- [Common Pitfalls](#5-common-pitfalls)
- [Example Programs](#6-example-programs)
- [How to Run the Code](#how-to-run-the-code)
- [Exam-Style Questions and Solutions](#exam-style-questions-and-solutions)
- [Contributing](#contributing)
- [License](#license)

## 1. Introduction to Control Structures

**Brief Explanation**: Control structures in C dictate the flow of program execution, allowing decisions, repetitions, and jumps. They include decision-making statements (`if`, `switch`), looping statements (`for`, `while`, `do-while`), and branching statements (`break`, `continue`, `return`). These constructs enable dynamic and efficient program behavior based on conditions and iterations.

**Real-World Context**: Control structures are used in applications like traffic light systems (decision-making for green/red), automated payroll systems (looping through employee records), and game logic (branching for player actions).

**Relation to `arithmetic_operations.c`**: Uses `if` to handle division by zero.

## 2. Decision Making Statements

**Brief Explanation**: Decision-making statements (`if`, `if-else`, `else-if`, `switch`) allow the program to execute specific code blocks based on conditions. They evaluate expressions to choose between alternative paths.

**Real-World Context**: Used in e-commerce for discount eligibility (e.g., `if` total > $100, apply discount) or vending machines (`switch` for item selection).

**Relation to `arithmetic_operations.c`**: Uses `if-else` to check if the divisor is zero.

## 3. Looping Statements

**Brief Explanation**: Looping statements (`for`, `while`, `do-while`) enable repeated execution of code blocks until a condition is met. `for` is ideal for known iteration counts, `while` for condition-based loops, and `do-while` for at least one execution.

**Real-World Context**: Used in inventory systems to process stock items (loop through quantities) or timers in appliances (repeat until time elapses).

**Relation to `arithmetic_operations.c`**: Could use loops for repeated calculations.

## 4. Branching Statements

**Brief Explanation**: Branching statements (`break`, `continue`, `return`) alter the flow within loops or functions. `break` exits a loop/switch, `continue` skips to the next iteration, and `return` exits a function with an optional value.

**Real-World Context**: Used in search algorithms (`break` when item found) or form validation (`continue` to skip invalid inputs).

**Relation to `arithmetic_operations.c`**: Uses `return` to end the `main` function.

## 5. Common Pitfalls

**Brief Explanation**: Common pitfalls include:
- **Infinite Loops**: Loops that never terminate (e.g., missing loop condition update).
- **Misplacement of Conditionals**: Incorrect placement of `if` or loop conditions leading to logical errors (e.g., wrong indentation or misplaced braces).

**Real-World Context**: Infinite loops can crash web servers; misplaced conditionals can cause incorrect billing in financial apps.

**Relation to `arithmetic_operations.c`**: Risk of logical errors if division-by-zero check is misplaced.

## 6. Example Programs

Below are over 20 example C programs demonstrating the concepts, including the `arithmetic_operations.c` program and additional programs with real-world applications. Each example includes code, purpose, and real-world context.

### Example 1: Arithmetic Operations (`arithmetic_operations.c`)
**Purpose**: Performs arithmetic operations on two user-input integers with division-by-zero check.
```c
#include <stdio.h>
int main() {
    int num1, num2;
    printf("Enter first number: ");
    scanf("%d", &num1);
    printf("Enter second number: ");
    scanf("%d", &num2);
    printf("Addition (+): %d + %d = %d\n", num1, num2, num1 + num2);
    printf("Subtraction (-): %d - %d = %d\n", num1, num2, num1 - num2);
    printf("Multiplication (*): %d * %d = %d\n", num1, num2, num1 * num2);
    if (num2 != 0) {
        printf("Division (/): %d / %d = %d\n", num1, num2, num1 / num2);
        printf("Modulus (%%): %d %% %d = %d\n", num1, num2, num1 % num2);
    } else {
        printf("Division (/): Cannot divide by zero\n");
        printf("Modulus (%%): Cannot perform modulus by zero\n");
    }
    return 0;
}
```
**Real-World Context**: Financial calculators for budgeting or expense tracking.

### Example 2: Discount Eligibility (`discount_check.c`)
**Purpose**: Checks if a purchase qualifies for a discount using `if-else`.
```c
#include <stdio.h>
int main() {
    float total;
    printf("Enter purchase total: ");
    scanf("%f", &total);
    if (total > 100) {
        printf("You qualify for a 10%% discount!\n");
    } else {
        printf("No discount applied.\n");
    }
    return 0;
}
```
**Real-World Context**: E-commerce platforms applying discounts.

### Example 3: Vending Machine Menu (`vending_menu.c`)
**Purpose**: Uses `switch` to select vending machine items.
```c
#include <stdio.h>
int main() {
    int choice;
    printf("Select item (1: Soda, 2: Chips, 3: Candy): ");
    scanf("%d", &choice);
    switch (choice) {
        case 1: printf("Dispensing Soda ($1.50)\n"); break;
        case 2: printf("Dispensing Chips ($1.00)\n"); break;
        case 3: printf("Dispensing Candy ($0.75)\n"); break;
        default: printf("Invalid choice\n");
    }
    return 0;
}
```
**Real-World Context**: Vending machine software.

### Example 4: Sum of Numbers (`sum_numbers.c`)
**Purpose**: Uses `for` loop to sum numbers from 1 to n.
```c
#include <stdio.h>
int main() {
    int n, sum = 0;
    printf("Enter a number: ");
    scanf("%d", &n);
    for (int i = 1; i <= n; i++) {
        sum += i;
    }
    printf("Sum of numbers from 1 to %d: %d\n", n, sum);
    return 0;
}
```
**Real-World Context**: Calculating total sales in retail.

### Example 5: Countdown Timer (`countdown.c`)
**Purpose**: Uses `while` loop for a countdown.
```c
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
```
**Real-World Context**: Quiz apps or kitchen timers.

### Example 6: Input Validation (`input_validation.c`)
**Purpose**: Uses `do-while` to ensure valid input.
```c
#include <stdio.h>
int main() {
    int rating;
    do {
        printf("Enter rating (1-5): ");
        scanf("%d", &rating);
    } while (rating < 1 || rating > 5);
    printf("Valid rating: %d\n", rating);
    return 0;
}
```
**Real-World Context**: Customer feedback forms.

### Example 7: Skip Invalid Input (`skip_invalid.c`)
**Purpose**: Uses `continue` to skip invalid inputs in a loop.
```c
#include <stdio.h>
int main() {
    int num;
    for (int i = 0; i < 5; i++) {
        printf("Enter a positive number: ");
        scanf("%d", &num);
        if (num <= 0) {
            printf("Invalid input, skipping...\n");
            continue;
        }
        printf("Accepted: %d\n", num);
    }
    return 0;
}
```
**Real-World Context**: Form validation in web apps.

### Example 8: Early Exit (`early_exit.c`)
**Purpose**: Uses `break` to exit a loop early.
```c
#include <stdio.h>
int main() {
    int num;
    while (1) {
        printf("Enter a number (0 to exit): ");
        scanf("%d", &num);
        if (num == 0) break;
        printf("You entered: %d\n", num);
    }
    printf("Exiting...\n");
    return 0;
}
```
**Real-World Context**: Search algorithms stopping when an item is found.

### Example 9: Function Return (`square_function.c`)
**Purpose**: Uses `return` to exit a function with a value.
```c
#include <stdio.h>
int square(int num) {
    return num * num;
}
int main() {
    int num;
    printf("Enter a number: ");
    scanf("%d", &num);
    printf("Square: %d\n", square(num));
    return 0;
}
```
**Real-World Context**: Mathematical utilities in engineering software.

### Example 10: Grade Calculator (`grade_calculator.c`)
**Purpose**: Uses `if-else` for grading based on marks.
```c
#include <stdio.h>
int main() {
    float marks;
    printf("Enter marks (0-100): ");
    scanf("%f", &marks);
    if (marks >= 90) printf("Grade: A\n");
    else if (marks >= 80) printf("Grade: B\n");
    else if (marks >= 70) printf("Grade: C\n");
    else printf("Grade: Fail\n");
    return 0;
}
```
**Real-World Context**: Educational grading systems.

### Example 11: Factorial (`factorial.c`)
**Purpose**: Uses `for` loop to calculate factorial.
```c
#include <stdio.h>
int main() {
    int n;
    unsigned long fact = 1;
    printf("Enter a number: ");
    scanf("%d", &n);
    for (int i = 1; i <= n; i++) {
        fact *= i;
    }
    printf("Factorial of %d: %lu\n", n, fact);
    return 0;
}
```
**Real-World Context**: Statistical calculations in data analysis.

### Example 12: Even Numbers (`even_numbers.c`)
**Purpose**: Uses `while` to print even numbers.
```c
#include <stdio.h>
int main() {
    int num = 2;
    while (num <= 10) {
        printf("%d ", num);
        num += 2;
    }
    printf("\n");
    return 0;
}
```
**Real-World Context**: Generating sequences in scheduling systems.

### Example 13: Menu Loop (`menu_loop.c`)
**Purpose**: Uses `do-while` for a menu-driven program.
```c
#include <stdio.h>
int main() {
    int choice;
    do {
        printf("1. Option 1\n2. Option 2\n3. Exit\nChoice: ");
        scanf("%d", &choice);
        switch (choice) {
            case 1: printf("Selected Option 1\n"); break;
            case 2: printf("Selected Option 2\n"); break;
            case 3: printf("Exiting...\n"); break;
            default: printf("Invalid choice\n");
        }
    } while (choice != 3);
    return 0;
}
```
**Real-World Context**: ATM or kiosk interfaces.

### Example 14: Sum of Digits (`sum_digits.c`)
**Purpose**: Uses `while` to sum digits of a number.
```c
#include <stdio.h>
int main() {
    int num, sum = 0;
    printf("Enter a number: ");
    scanf("%d", &num);
    while (num > 0) {
        sum += num % 10;
        num /= 10;
    }
    printf("Sum of digits: %d\n", sum);
    return 0;
}
```
**Real-World Context**: Checksum calculations in data validation.

### Example 15: Prime Number Check (`prime_check.c`)
**Purpose**: Uses `for` and `if` to check if a number is prime.
```c
#include <stdio.h>
int main() {
    int num, is_prime = 1;
    printf("Enter a number: ");
    scanf("%d", &num);
    for (int i = 2; i * i <= num; i++) {
        if (num % i == 0) {
            is_prime = 0;
            break;
        }
    }
    if (is_prime && num > 1) printf("%d is prime\n", num);
    else printf("%d is not prime\n", num);
    return 0;
}
```
**Real-World Context**: Cryptography algorithms.

### Example 16: Infinite Loop Example (`infinite_loop.c`)
**Purpose**: Demonstrates an infinite loop (pitfall).
```c
#include <stdio.h>
int main() {
    int i = 0;
    while (i < 5) {
        printf("This will run forever!\n");
        // Missing i++ causes infinite loop
    }
    return 0;
}
```
**Real-World Context**: Can crash servers if not fixed.

### Example 17: Misplaced Conditional (`misplaced_conditional.c`)
**Purpose**: Shows incorrect conditional placement (pitfall).
```c
#include <stdio.h>
int main() {
    int num = 10;
    if (num > 5);
        printf("This will always print!\n"); // Misplaced semicolon
    return 0;
}
```
**Real-World Context**: Causes logical errors in billing systems.

### Example 18: Traffic Light (`traffic_light.c`)
**Purpose**: Uses `switch` for traffic light states.
```c
#include <stdio.h>
int main() {
    int state;
    printf("Enter light state (1: Red, 2: Yellow, 3: Green): ");
    scanf("%d", &state);
    switch (state) {
        case 1: printf("Stop\n"); break;
        case 2: printf("Prepare\n"); break;
        case 3: printf("Go\n"); break;
        default: printf("Invalid state\n");
    }
    return 0;
}
```
**Real-World Context**: Traffic light control systems.

### Example 19: Multiplication Table (`multiplication_table.c`)
**Purpose**: Uses nested `for` loops for a multiplication table.
```c
#include <stdio.h>
int main() {
    for (int i = 1; i <= 5; i++) {
        for (int j = 1; j <= 5; j++) {
            printf("%d ", i * j);
        }
        printf("\n");
    }
    return 0;
}
```
**Real-World Context**: Educational tools for math.

### Example 20: Odd Number Sum (`odd_sum.c`)
**Purpose**: Uses `for` and `if` to sum odd numbers.
```c
#include <stdio.h>
int main() {
    int sum = 0;
    for (int i = 1; i <= 10; i++) {
        if (i % 2 != 0) sum += i;
    }
    printf("Sum of odd numbers from 1 to 10: %d\n", sum);
    return 0;
}
```
**Real-World Context**: Data filtering in analytics.

### Example 21: Number Guessing Game (`guess_number.c`)
**Purpose**: Uses `do-while` and `if` for a game.
```c
#include <stdio.h>
int main() {
    int secret = 7, guess;
    do {
        printf("Guess the number (1-10): ");
        scanf("%d", &guess);
        if (guess == secret) {
            printf("Correct!\n");
            break;
        } else {
            printf("Try again\n");
        }
    } while (1);
    return 0;
}
```
**Real-World Context**: Interactive games or quizzes.

### Example 22: Positive Number Counter (`positive_counter.c`)
**Purpose**: Uses `while` and `break` to count positive inputs.
```c
#include <stdio.h>
int main() {
    int num, count = 0;
    while (1) {
        printf("Enter a number (0 to stop): ");
        scanf("%d", &num);
        if (num == 0) break;
        if (num > 0) count++;
    }
    printf("Positive numbers entered: %d\n", count);
    return 0;
}
```
**Real-World Context**: Survey systems counting valid responses.

## How to Run the Code

**Prerequisites**:
- Install `gcc` (e.g., on macOS: `brew install gcc`, on Ubuntu: `sudo apt-get install gcc`).
- Use a terminal and text editor/IDE (e.g., Visual Studio Code, Code::Blocks).

**Steps**:
1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-directory>
   ```
2. Compile a program (e.g., `arithmetic_operations.c`):
   ```bash
   gcc arithmetic_operations.c -o arithmetic_operations
   ```
3. Run:
   ```bash
   ./arithmetic_operations
   ```
4. For other examples, save the code as `.c` files (e.g., `discount_check.c`), compile, and run similarly:
   ```bash
   gcc discount_check.c -o discount_check
   ./discount_check
   ```

**Example Output** (for `arithmetic_operations.c`):
```
Enter first number: 10
Enter second number: 5
Addition (+): 10 + 5 = 15
Subtraction (-): 10 - 5 = 5
Multiplication (*): 10 * 5 = 50
Division (/): 10 / 5 = 2
Modulus (%): 10 % 5 = 0
```

## Exam-Style Questions and Solutions

Below are 20+ exam-style questions with solutions to reinforce understanding of control structures.

### Question 1
**Write a C program to check if a number is even or odd using `if-else`.**
**Solution**:
```c
#include <stdio.h>
int main() {
    int num;
    printf("Enter a number: ");
    scanf("%d", &num);
    if (num % 2 == 0) printf("%d is even\n", num);
    else printf("%d is odd\n", num);
    return 0;
}
```

### Question 2
**Write a program to print the first 10 natural numbers using a `for` loop.**
**Solution**:
```c
#include <stdio.h>
int main() {
    for (int i = 1; i <= 10; i++) {
        printf("%d ", i);
    }
    printf("\n");
    return 0;
}
```

### Question 3
**Write a program to find the largest of three numbers using `if-else`.**
**Solution**:
```c
#include <stdio.h>
int main() {
    int a, b, c;
    printf("Enter three numbers: ");
    scanf("%d %d %d", &a, &b, &c);
    if (a >= b && a >= c) printf("Largest: %d\n", a);
    else if (b >= a && b >= c) printf("Largest: %d\n", b);
    else printf("Largest: %d\n", c);
    return 0;
}
```

### Question 4
**Write a program to calculate the sum of digits of a number using a `while` loop.**
**Solution**:
```c
#include <stdio.h>
int main() {
    int num, sum = 0;
    printf("Enter a number: ");
    scanf("%d", &num);
    while (num > 0) {
        sum += num % 10;
        num /= 10;
    }
    printf("Sum of digits: %d\n", sum);
    return 0;
}
```

### Question 5
**Write a program to print a menu using `switch` and exit on user choice.**
**Solution**:
```c
#include <stdio.h>
int main() {
    int choice;
    printf("1. Start\n2. Stop\n3. Exit\nChoice: ");
    scanf("%d", &choice);
    switch (choice) {
        case 1: printf("Starting...\n"); break;
        case 2: printf("Stopping...\n"); break;
        case 3: printf("Exiting...\n"); break;
        default: printf("Invalid choice\n");
    }
    return 0;
}
```

### Question 6
**Write a program to count even numbers from 1 to n using a `for` loop.**
**Solution**:
```c
#include <stdio.h>
int main() {
    int n, count = 0;
    printf("Enter a number: ");
    scanf("%d", &n);
    for (int i = 1; i <= n; i++) {
        if (i % 2 == 0) count++;
    }
    printf("Even numbers: %d\n", count);
    return 0;
}
```

### Question 7
**Write a program to reverse a number using a `while` loop.**
**Solution**:
```c
#include <stdio.h>
int main() {
    int num, rev = 0;
    printf("Enter a number: ");
    scanf("%d", &num);
    while (num > 0) {
        rev = rev * 10 + num % 10;
        num /= 10;
    }
    printf("Reverse: %d\n", rev);
    return 0;
}
```

### Question 8
**Write a program to check if a number is positive, negative, or zero using `if-else`.**
**Solution**:
```c
#include <stdio.h>
int main() {
    int num;
    printf("Enter a number: ");
    scanf("%d", &num);
    if (num > 0) printf("Positive\n");
    else if (num < 0) printf("Negative\n");
    else printf("Zero\n");
    return 0;
}
```

### Question 9
**Write a program to print Fibonacci series up to n terms using a `for` loop.**
**Solution**:
```c
#include <stdio.h>
int main() {
    int n, a = 0, b = 1, c;
    printf("Enter number of terms: ");
    scanf("%d", &n);
    printf("Fibonacci: %d %d ", a, b);
    for (int i = 3; i <= n; i++) {
        c = a + b;
        printf("%d ", c);
        a = b;
        b = c;
    }
    printf("\n");
    return 0;
}
```

### Question 10
**Write a program to validate age (18-60) using a `do-while` loop.**
**Solution**:
```c
#include <stdio.h>
int main() {
    int age;
    do {
        printf("Enter age (18-60): ");
        scanf("%d", &age);
    } while (age < 18 || age > 60);
    printf("Valid age: %d\n", age);
    return 0;
}
```

### Question 11
**Write a program to skip multiples of 3 in a loop using `continue`.**
**Solution**:
```c
#include <stdio.h>
int main() {
    for (int i = 1; i <= 10; i++) {
        if (i % 3 == 0) continue;
        printf("%d ", i);
    }
    printf("\n");
    return 0;
}
```

### Question 12
**Write a program to exit a loop when a negative number is entered using `break`.**
**Solution**:
```c
#include <stdio.h>
int main() {
    int num;
    while (1) {
        printf("Enter a number: ");
        scanf("%d", &num);
        if (num < 0) break;
        printf("You entered: %d\n", num);
    }
    printf("Negative number entered, exiting...\n");
    return 0;
}
```

### Question 13
**Write a program to calculate power (base, exponent) using a `for` loop.**
**Solution**:
```c
#include <stdio.h>
int main() {
    int base, exp, result = 1;
    printf("Enter base and exponent: ");
    scanf("%d %d", &base, &exp);
    for (int i = 1; i <= exp; i++) {
        result *= base;
    }
    printf("%d^%d = %d\n", base, exp, result);
    return 0;
}
```

### Question 14
**Write a program to check if a year is a leap year using `if-else`.**
**Solution**:
```c
#include <stdio.h>
int main() {
    int year;
    printf("Enter a year: ");
    scanf("%d", &year);
    if ((year % 4 == 0 && year % 100 != 0) || (year % 400 == 0))
        printf("%d is a leap year\n", year);
    else
        printf("%d is not a leap year\n", year);
    return 0;
}
```

### Question 15
**Write a program to print a pattern of stars using nested `for` loops.**
**Solution**:
```c
#include <stdio.h>
int main() {
    for (int i = 1; i <= 5; i++) {
        for (int j = 1; j <= i; j++) {
            printf("* ");
        }
        printf("\n");
    }
    return 0;
}
```

### Question 16
**Write a program to find GCD of two numbers using a `while` loop.**
**Solution**:
```c
#include <stdio.h>
int main() {
    int a, b, temp;
    printf("Enter two numbers: ");
    scanf("%d %d", &a, &b);
    while (b != 0) {
        temp = b;
        b = a % b;
        a = temp;
    }
    printf("GCD: %d\n", a);
    return 0;
}
```

### Question 17
**Write a program to simulate a simple calculator using `switch`.**
**Solution**:
```c
#include <stdio.h>
int main() {
    char op;
    float a, b;
    printf("Enter operator (+, -, *, /): ");
    scanf(" %c", &op);
    printf("Enter two numbers: ");
    scanf("%f %f", &a, &b);
    switch (op) {
        case '+': printf("Result: %.2f\n", a + b); break;
        case '-': printf("Result: %.2f\n", a - b); break;
        case '*': printf("Result: %.2f\n", a * b); break;
        case '/': 
            if (b != 0) printf("Result: %.2f\n", a / b);
            else printf("Cannot divide by zero\n");
            break;
        default: printf("Invalid operator\n");
    }
    return 0;
}
```

### Question 18
**Write a program to count vowels in a string using a `for` loop.**
**Solution**:
```c
#include <stdio.h>
int main() {
    char str[50];
    int count = 0;
    printf("Enter a string: ");
    scanf("%s", str);
    for (int i = 0; str[i] != '\0'; i++) {
        if (str[i] == 'a' || str[i] == 'e' || str[i] == 'i' || 
            str[i] == 'o' || str[i] == 'u')
            count++;
    }
    printf("Vowels: %d\n", count);
    return 0;
}
```

### Question 19
**Write a program to demonstrate an infinite loop pitfall and fix it.**
**Solution**:
```c
#include <stdio.h>
int main() {
    int i = 0;
    while (i < 5) {
        printf("%d ", i);
        i++; // Fix: Increment to avoid infinite loop
    }
    printf("\n");
    return 0;
}
```

### Question 20
**Write a program to fix a misplaced conditional pitfall.**
**Solution**:
```c
#include <stdio.h>
int main() {
    int num = 10;
    if (num > 5) { // Fix: Remove semicolon and add braces
        printf("Number is greater than 5\n");
    }
    return 0;
}
```

### Question 21
**Write a program to print numbers divisible by 5 using a `for` loop.**
**Solution**:
```c
#include <stdio.h>
int main() {
    for (int i = 1; i <= 50; i++) {
        if (i % 5 == 0) printf("%d ", i);
    }
    printf("\n");
    return 0;
}
```

### Question 22
**Write a program to simulate a login system with limited attempts using a `do-while` loop.**
**Solution**:
```c
#include <stdio.h>
int main() {
    int password = 1234, input, attempts = 3;
    do {
        printf("Enter password (%d attempts left 3 remaining): ");
        scanf("%d", &input);
        if (input == password) {
            printf("Login successful\n");
            break;
        } else {
            printf("Incorrect password\n");
            attempts--;
        }
    } while (attempts > 0);
    if (attempts == 0) printf("Too many failed attempts\n");
    return 0;
}
```

## Contributing

Contributions are welcome! You can:
- Add more C programs demonstrating control structures.
- Enhance examples with new real-world scenarios.
- Improve the README with additional details or questions.

To contribute:
1. Fork the repository.
2. Create a branch:
   ```bash
   git checkout -b feature-branch
   ```
3. Commit changes:
   ```bash
   git commit -m "Add feature"
   ```
4. Push:
   ```bash
   git push origin feature-branch
   ```
5. Open a pull request.
