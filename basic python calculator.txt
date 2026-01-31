import math

# Core arithmetic functions
def add(x, y):
    return x + y

def subtract(x, y):
    return x - y

def multiply(x, y):
    return x * y

def divide(x, y):
    try:
        return x / y
    except ZeroDivisionError:
        return "Error: Cannot divide by zero."

def power(x, y):
    return math.pow(x, y)

def square_root(x):
    try:
        return math.sqrt(x)
    except ValueError:
        return "Error: Cannot take square root of a negative number."

# User Interface
def display_menu():
    print("\nSimple Python Calculator")
    print("------------------------")
    print("1. Addition")
    print("2. Subtraction")
    print("3. Multiplication")
    print("4. Division")
    print("5. Power")
    print("6. Square Root")
    print("0. Exit")

def get_number(prompt):
    while True:
        try:
            return float(input(prompt))
        except ValueError:
            print("Invalid input. Please enter a number.")

# Main calculator logic
def calculator():
    while True:
        display_menu()
        choice = input("Enter your choice (0-6): ")

        if choice == '0':
            print("Thank you for using the calculator. Goodbye!")
            break

        if choice in ['1', '2', '3', '4', '5']:
            num1 = get_number("Enter first number: ")
            num2 = get_number("Enter second number: ")

            operations = {
                '1': add,
                '2': subtract,
                '3': multiply,
                '4': divide,
                '5': power
            }

            result = operations[choice](num1, num2)
            print("Result:", result)

        elif choice == '6':
            num = get_number("Enter a number: ")
            print("Result:", square_root(num))

        else:
            print("Invalid choice. Please try again.")

# Entry point
if __name__ == "__main__":
    calculator()
