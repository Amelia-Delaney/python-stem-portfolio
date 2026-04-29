**Name:** Amelia Delaney
**School:** Bishops Stortford College
**Course:** python for STEM
**Year:** Year 12, 2026-2027

## About Me

I plan on studying engineering at university in 2027. I am currently studying Alevel physics, maths, further maths, and economics and plan on acheiving 3 A* and an A in further maths at the end of year 13.



# course overview

This portfolio documents my progress through a Python programming course designed for students preparing for STEM pathways at university. The course covers:

Python fundamentals (variables, input/output, data types)
- Control structures (loops and conditionals)
- Functions and modular code
- Data structures (lists, dictionaries, tuples, sets)
- Validation and error handling
- File handling
- Object-Oriented Programming (OOP)
- Version control with Git and GitHub
- Working with Jupyter Notebooks

# Portfolio Projects

| # | Project | Key Skills | Status |
|---|---|---|---|
| 1 | [Unit Converter](#unit-converter) | Variables, functions, input/output | ✅ Complete |
| 2 | [Number Guessing Game](#) | Loops, conditionals, random | ✅ Complete |
| 3 | [To-Do List](#) | Lists, functions, data structures | ✅ Complete |
| 4 | [Student Grade Calculator](#) | Dictionaries, validation, error handling | ✅ Complete |
| 5 | [OOP Bank Account](#) | Classes, OOP principles | ✅ Complete |
| 6 | [Data Analysis Notebook](#) | Jupyter Notebooks, data exploration | ✅ Complete |

## Skills I Have Developed

**Programming Concepts**
- Writing clean, well-commented Python code
- Using functions to organise and reuse code
- Handling user input safely with validation

**Tools and Technologies**
- Python 3 (Thonny IDE)
- Jupyter Notebooks
- Git version control
- GitHub for code sharing and portfolio management
- Markdown for documentation

## Contact

- **GitHub:** [Amelia Delaney]
- **Email:** [26delana@bscmail.org]

# Projects

## Unit Converter

**Description**

waffle about code

**Code**

```python
def km_to_miles(km):
    """Convert kilometres to miles."""
    miles = km * 0.621371
    return miles

def miles_to_km(miles):
    """Convert miles to kilometres."""
    km = miles / 0.621371
    return km

def celsius_to_fahrenheit(celsius):
    """Convert celsius to fahrenheit"""
    fahrenheit = celsius * 3.38
    return fahrenheit

def fahrenheit_to_celsius(fahrenheit):
    """Convert celsius to fahrenheit"""
    celsius = fahrenheit /3.38
    return celsius

def show_menu():
    print("=== Unit Converter ===")
    print("1. Kilometres to Miles")
    print("2. Miles to Kilometres")
    print("3. Celsius to Fahrenheit")
    print("4. Fahrenheit to Celsius")

def main():
    show_menu()
    choice = input("Enter your choice (1-4): ")
    
    if choice == "1":
        km = float(input("Enter kilometres: "))
        result = km_to_miles(km)
        print(f"{km} km = {result:.2f} miles")
        
    elif choice == "2":
        miles = float(input("Enter miles: "))
        result = miles_to_km(miles)
        print(f"{miles} miles = {result:.2f} km")
    
    elif choice == "3":
        celsius = float(input("Enter celcius: "))
        result = celsius_to_fahrenheit(celsius)
        print(f"{celsius} celsius = {result:.2f} fahrenheit")
        
    elif choice == "4":
        fahrenheit = float(input("Enter fahrenheit: "))
        result = fahrenheit_to_celsius(fahrenheit)
        print(f"{fahrenheit} fahrenheit = {result:.2f} celsius")

main()'''