def add(x, y):
    return x + y
def subtract(x, y):
    return x - y
def multiply(x, y):
    return x * y
def divide(x, y):
    if y == 0:
        return "Error! Division by zero."
    return x / y

def modulus(x, y):
    return x % y
def power(x, y):
    return x ** y
def calculator():
    while True:
        print("\nSelect operation:")
        print("1. Add")
        print("2. Subtract")
        print("3. Multiply")
        print("4. Divide")
        print("5. Modulus")
        print("6. Power")
        print("7. Exit")

        choice = input("Enter choice (1/2/3/4/5/6/7): ")
        if choice == '7':
            print("Exiting the calculator. Goodbye!")
            break
        if choice in ('1', '2', '3', '4', '5', '6'):
            try:
                num1 = float(input("Enter first number: "))
                num2 = float(input("Enter second number: "))
            except ValueError:
                print("Invalid input! Please enter numeric values.")
                continue
        if choice == '1':
                print(f"The result is: {add(num1, num2)}")
        elif choice == '2':
                print(f"The result is: {subtract(num1, num2)}")
        elif choice == '3':
                print(f"The result is: {multiply(num1, num2)}")
        elif choice == '4':
                print(f"The result is: {divide(num1, num2)}")
        elif choice == '5':
                print(f"The result is: {modulus(num1, num2)}")
        elif choice == '6':
                print(f"The result is: {power(num1, num2)}")
        else:
            print("Invalid choice! Please select a valid option.")

if _name_ == "_main_":
    calculator()
