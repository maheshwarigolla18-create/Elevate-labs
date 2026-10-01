# Calculator CLI App

A simple command-line calculator built with Python. It supports addition, subtraction, multiplication and division.

## Features

- Separate function logic for each operation (+, -, *, /)
- Takes user input with `input()`
- Handles division by zero
- Handles invalid operators
- Loops until the user chooses to exit

## Requirements

- Python 3.x
- VS Code or any text editor, and a terminal

## How to Run

```bash
python calculator.py
```

## Code

```python
def calculate(a, op, b):
    if op == "+":
        return a + b
    elif op == "-":
        return a - b
    elif op == "*":
        return a * b
    elif op == "/":
        return "Cannot divide by zero" if b == 0 else a / b
    return "Invalid operator"

while True:
    a = float(input("Enter first number: "))
    op = input("Enter operator (+, -, *, /): ")
    b = float(input("Enter second number: "))
    print("Result:", calculate(a, op, b))

    if input("Calculate again? (y/n): ").lower() != "y":
        print("Goodbye!")
        break
```

## Sample Output

```
Enter first number: 10
Enter operator (+, -, *, /): +
Enter second number: 5
Result: 15.0
Calculate again? (y/n): y
Enter first number: 20
Enter operator (+, -, *, /): *
Enter second number: 5
Result: 100.0
Calculate again? (y/n): y
Enter first number: 8
Enter operator (+, -, *, /): /
Enter second number: 0
Result: Cannot divide by zero
Calculate again? (y/n): n
Goodbye!
```

## Key Concepts

Functions, Loops, Conditionals, CLI Interaction

## Author

Your Name
