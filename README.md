# To-Do-List-task2.py

Task 2 : Create a To-Do List Application (Console-based) :
To-Do List CLI App (Python)
This is a simple command-line To-Do List application built in Python. It allows users to add, view, and remove tasks using a menu-driven interface. Tasks are saved in a file, so they remain even after restarting the program.

Features
•	Add tasks
•	View all tasks
•	Remove tasks
•	Tasks are saved in tasks.txt for persistence
•	Input validation to avoid crashes
•	Menu-driven CLI using a loop
•	Modular code using functions

How to Run
1.	Make sure you have Python installed.
2.	Save the file as todo.py
3.	Open your terminal or PowerShell.
4.	Navigate to the folder where todo.py is saved:
cd path\to\your\folder
5.	Run the program:
python todo.py

Code Explanation:

1. Function Definitions
def load_tasks():
    ...

def save_tasks(tasks):
    ...

def add_task(task):
    ...

def remove_task(index):
    ...

def view_tasks():
    ...
•	load_tasks(): Reads tasks from tasks.txt into a list.
•	save_tasks(tasks): Saves the current list of tasks to the file.
•	add_task(task): Adds a new task to the list.
•	remove_task(index): Deletes a task based on its number.
•	view_tasks(): Shows all the tasks with numbering.
These functions keep the code modular, clean, and reusable.

2. Menu Interface
def show_menu():
    print("1. View Tasks")
    print("2. Add Task")
    print("3. Remove Task")
    print("4. Exit")
•	Displays user options.
•	Called in a loop so the menu keeps showing after each action.

3. Main To-Do List Loop
def main():
    while True:
        show_menu()
        choice = input("Choose an option (1-4): ")

        if choice == '1':
            view_tasks()
        elif choice == '2':
            task = input("Enter the task: ")
            add_task(task)
        elif choice == '3':
            view_tasks()
            try:
                task_num = int(input("Enter task number to remove: ")) - 1
                remove_task(task_num)
            except ValueError:
                print("Please enter a valid number.")
        elif choice == '4':
            print("Goodbye!")
            break
        else:
            print("Invalid choice.")
•	Uses a while True loop to keep the program running until the user chooses Exit (4).
•	Gets user input and calls the appropriate function.
•	Handles errors for invalid choices and non-numeric input during task removal.

4. Main Entry Point
if __name__ == "__main__":
    main()
•	This line ensures the app runs only when you execute todo.py directly.
•	It prevents the app from running if the file is imported somewhere else.


Sample output when run in terminal using powershell (refer the docx file for the sample output to view):
 
Navigate to the folder where task2.py is saved and run:
 
The option displays for user to select operation. Choose either View Tasks, Add Task, Remove Task or Exit. 
So, I chose option 1 to View Tasks. The output is displayed which are manreenyaseen and vamshi.

Next, I chose option 2 to Add Task. Add the task sheikh.
 
Next, I chose option 1 to view task The output is displayed which are manreenyaseen, vamshi, and sheikh.
 
Next, I chose option 3 to Remove Task. So remove 2 which is vamshi.
 
Then choose option 3 to View Tasks. It displays manreenyaseen and sheikh only because vamshi is removed.

Then choose option 4 to Exit. The output will display Goodbye
