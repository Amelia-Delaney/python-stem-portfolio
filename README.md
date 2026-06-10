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
| 2 | [Number Guessing Game](#number-guessing-game) | Loops, conditionals, random | ✅ Complete |
| 3 | [To-Do List](#to-do-list) | Lists, functions, data structures | ✅ Complete |
| 4 | [Student Grade Calculator](#student-grade-calculator) | Dictionaries, validation, error handling | ✅ Complete |
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

This code enables the user to choose a converter from the menu. By inputing the designated number e.g. 1, they are able to convert between Kilometers and Miles by inputing the number of Kilometers they want to convert. The code will then print the correspoding number of miles.

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

main()```

## Number Guessing Game

**Description**

This code enables the user to choose the desired game difficulty level from a menu with the options of guessing a number between 1-50, 1-100 and 1-500. The user is then asked to input a number they think the computer has chosen. The code then prints whether the users number is higher or lower than the chosen number and the user has to keep playing until they guess the correct number. Once the level is completed, the user is asked whether they want to play again.

**Code**

```python
def show_menu():
    print("=== Number Guessing Game ===")
    print("1. Easy 1-50")
    print("2. Medium 1-100")
    print("3. Hard 1-500")

def main():
    show_menu()
    choice = input("Enter your choice (1-3): ")

    if choice == "1":
        import random
        secret = random.randint(1, 50)
        attempts = 0
            
        print("I'm thinking of a number between 1 and 50.")
            
        while True:
            guess = int(input("Your guess: "))
            attempts += 1
            
            if guess < secret:
                print("Too low! Try again.")
            elif guess > secret:
                print("Too high! Try again.")
            else:
                print(f"Correct! You got it in {attempts} attempts.")
                response = (input("do you want to play again:"))
                if response.lower() == 'yes':
                    continue
                elif response.lower() == 'no':
                    break  # Exit the loop
            
    if choice == "2":
        import random
        secret = random.randint(1, 100)
        attempts = 0
        
        print("I'm thinking of a number between 1 and 100.")
        
        while True:
            guess = int(input("Your guess: "))
            attempts += 1
            
            if guess < secret:
                print("Too low! Try again.")
            elif guess > secret:
                print("Too high! Try again.")
            else:
                print(f"Correct! You got it in {attempts} attempts.")
                response = (input("do you want to play again:"))
                if response.lower() == 'yes':
                    continue
                elif response.lower() == 'no':
                    break  # Exit the loop
            
    if choice == "3":
        import random

           
        secret = random.randint(1, 500)
        attempts = 0
        
        print("I'm thinking of a number between 1 and 500.")
        
        while True:
            guess = int(input("Your guess: "))
            attempts += 1
            
            if guess < secret:
                print("Too low! Try again.")
            elif guess > secret:
                print("Too high! Try again.")
            else:
                print(f"Correct! You got it in {attempts} attempts.")
                response = (input("do you want to play again:"))
                if response.lower() == 'yes':
                    continue
                elif response.lower() == 'no':
                    break  # Exit the loop

main()```

## To Do List

**Description**

This code enables the user access a To Do List menu. The user is able to 1 View tasks, 2 Add tasks, 3 Mark a task as done, 4 remove a task or 5 Quit. By inputing the corresponding number the user is able to carry out the specific function. When entereing 1 and viewing tasks, the user can see their tasks in a neat table with the first task they entered labelled 1, and the last task they entered labelled the number of tasks in the table.

**Code**

```python
def show_tasks(tasks):
    """Display all tasks with their numbers and done status."""
    if len(tasks) == 0:
        print("No tasks yet!")
        return
    
    print("\n=== Your Tasks ===")
    for i, task in enumerate(tasks, start=1):
        status = "✓" if task["done"] else " "
        print(f"{i}. [{status}] {task['name']}")
    print()


def add_task(tasks):
    """Add a new task to the list."""
    new_task = input("Enter task: ")
    tasks.append({"name": new_task, "done": False})
    print(f"Added: '{new_task}'")


def mark_done(tasks):
    """Mark a task as done."""
    show_tasks(tasks)
    number = int(input("Enter task number to mark as done: "))
    
    if 1 <= number <= len(tasks):
        tasks[number - 1]["done"] = True
        print(f"Marked as done: '{tasks[number - 1]['name']}'")
    else:
        print("Invalid number.")


def remove_task(tasks):
    """Remove a task by number."""
    show_tasks(tasks)
    number = int(input("Enter task number to remove: "))
    
    if 1 <= number <= len(tasks):
        removed = tasks.pop(number - 1)
        print(f"Removed: '{removed['name']}'")
    else:
        print("Invalid number.")


def main():
    tasks = []
    
    while True:
        print("=== To-Do List ===")
        print("1. View tasks")
        print("2. Add task")
        print("3. Mark task as done")
        print("4. Remove task")
        print("5. Quit")
        
        choice = input("Choose: ")
        
        if choice == "1":
            show_tasks(tasks)
        elif choice == "2":
            add_task(tasks)
        elif choice == "3":
            mark_done(tasks)
        elif choice == "4":
            remove_task(tasks)
        elif choice == "5":
            print("Goodbye!")
            break


main()```



## Student Grade Calculator

**Description**

This code asks the user to input the name of a student for example Mary and their score in Maths, English and Science. Using these scores, the code prints the scores in a neat table titled Results for Mary, with their average percentage and overall letter grade printed beneath. The user is then asked if they wish to enter another student into the code

**Code**

```python
def get_grade(average):
    """Return a letter grade based on average percentage."""
    if average >= 70:
        return "A"
    elif average >= 60:
        return "B"
    elif average >= 50:
        return "C"
    elif average >= 40:
        return "D"
    else:
        return "U"

def get_valid_score(subject):
    """Ask for a score and keep asking until a valid number is entered."""
    while True:
        try:
            score = float(input(f"Enter score for {subject} (0-100): "))
            if 0 <= score <= 100:
                return score
            else:
                print("Score must be between 0 and 100.")
        except ValueError:
            print("Please enter a number.")

def calculate_results():
    """Collect scores and display results."""
    name = input("Student name: ")
    subjects = ["Maths", "English", "Science"]
    scores = {}
    
    for subject in subjects:
        scores[subject] = get_valid_score(subject)
    
    average = sum(scores.values()) / len(scores)
    grade = get_grade(average)
    
    print(f"\n=== Results for {name} ===")
    for subject, score in scores.items():
        print(f"  {subject}: {score:.1f}")
    print(f"Average: {average:.1f}%")
    print(f"Grade: {grade}")
    
while True:
    calculate_results()
    calculate_resultsagain = input('Would you like to add another student?:')
    if calculate_resultsagain == "yes":
        continue
    else: break
calculate_results()```

