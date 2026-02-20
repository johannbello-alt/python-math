# python-math
helps you with math
python
import math

def display_menu():
    print("\n--- 🧮 Math Homework Helper ---")
    print("1. Basic Arithmetic (+, -, *, /)")
    print("2. Area of a Circle")
    print("3. Pythagorean Theorem (Find Hypotenuse)")
    print("4. Solve for X (Simple Linear: ax + b = 0)")
    print("5. Exit")

def solve_linear():
    print("\nFormat: ax + b = 0")
    a = float(input("Enter value for a: "))
    b = float(input("Enter value for b: "))
    if a == 0:
        print("Invalid equation (a cannot be 0).")
    else:
        # Step: ax = -b  => x = -b / a
        result = -b / a
        print(f"✅ Result: x = {result}")

def pythagoras():
    a = float(input("Enter side a: "))
    b = float(input("Enter side b: "))
    c = math.sqrt(a**2 + b**2)
    print(f"✅ The hypotenuse (c) is: {round(c, 2)}")

def main():
    while True:
        display_menu()
        choice = input("\nWhat are we working on today? (1-5): ")

        if choice == '1':
            expr = input("Enter your expression (e.g., 10 * 5 / 2): ")
            print(f"✅ Result: {eval(expr)}")
        elif choice == '2':
            r = float(input("Enter radius: "))
            area = math.pi * (r**2)
            print(f"✅ Area: {round(area, 2)}")
        elif choice == '3':
            pythagoras()
        elif choice == '4':
            solve_linear()
        elif choice == '5':
            print("Good luck with your studies! 👋")
            break
        else:
            print("Invalid choice, try again.")

if __name__ == "__main__":
    main()
