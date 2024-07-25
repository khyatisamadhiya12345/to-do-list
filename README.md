# to-do-list
Developed a to-do list by using python basic operations. In this we make to-do list by using the functions of list and functions. Using lists and basic functions.
# To-Do List Application

# Initialize an empty list to store tasks
tasks = []

# Function to display the menu
def display_menu():
    print("To-Do List Application")
    print("1. Add a Task")
    print("2. View Tasks")
    print("3. Delete a Task")
    print("4. Exit")

# Function to add a task
def add_task():
    task = input("Enter the task: ")
    tasks.append(task)
    print(f"Task '{task}' added.")

# Function to view tasks
def view_tasks():
    if not tasks:
        print("No tasks to show.")
    else:
        print("Tasks:")
        for i, task in enumerate(tasks, 1):
            print(f"{i}. {task}")

# Function to delete a task
def delete_task():
    view_tasks()
    if tasks:
        task_num = int(input("Enter the task number to delete: "))
        if 0 < task_num <= len(tasks):
            task = tasks.pop(task_num - 1)
            print(f"Task '{task}' deleted.")
        else:
            print("Invalid task number.")

# Main loop
while True:
    display_menu()
    choice = input("Choose an option (1-4): ")

    if choice == '1':
        add_task()
    elif choice == '2':
        view_tasks()
    elif choice == '3':
        delete_task()
    elif choice == '4':
        print("Exiting the application. Goodbye!")
        break
    else:
        print("Invalid choice. Please choose a valid option.")
