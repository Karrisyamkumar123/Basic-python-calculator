
This README.md provides a clear overview of your Python-based calculator, explaining its functionality, structure, and how to run it.

Simple Python Calculator
A clean, functional command-line calculator built with Python. This tool handles basic arithmetic and specialized mathematical operations like powers and square roots with built-in error handling for common mathematical constraints.

Features
Basic Arithmetic: Support for addition, subtraction, multiplication, and division.

Advanced Math: Calculate powers (x 
y
 ) and square roots ( 
x

​
 ) using the Python math library.

Error Handling:

Prevents crashes from division by zero.

Handles invalid inputs for square roots (negative numbers).

Validates user input to ensure only numeric values are processed.

Interactive Menu: A simple loop-based interface that allows for multiple calculations in a single session.

Logic Flow
The application follows a standard modular structure to separate logic from the user interface:

Core Functions: Individual functions for each math operation (add, subtract, etc.).

Input Validation: The get_number function ensures the program doesn't crash if a user types text instead of a digit.

Main Loop: The calculator function manages the state and routes user choices to the correct operation.

How to Use
1. Requirements
Python 3.x installed on your machine.

2. Installation
Clone or download the main.py file to your local directory.

3. Running the Program
Open your terminal or command prompt and execute:

Bash
python main.py
4. Operations
Once the menu appears, enter a number (0-6) to select an operation:

1-4: Basic Math (+, -, *, /)

5: Power (Base and Exponent)

6: Square Root

0: Exit the program

Technical Details
The program utilizes the following Python features:

math Module: Used for precise power and square root calculations.

Dictionary Mapping: Uses a dictionary to map user input keys to function objects for efficient operation selection.

Exception Handling: Employs try-except blocks to catch ZeroDivisionError and ValueError.
