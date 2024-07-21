tasks = {}


def add_task():
    task_name = input("Enter task: ")
    tasks[len(tasks) + 1] = task_name
    print(f"Task '{task_name}' added.")


def delete_task():
    task_number = int(input("Enter task number to delete: "))
    if task_number in tasks:
        deleted_task = tasks.pop(task_number)
        print(f"Task '{deleted_task}' deleted.")
    else:
        print("Invalid task number.")

def view_tasks():
    if tasks:
        print("Tasks:")
        for number, task in tasks.items():
            print(f"{number}: {task}")
    else:
        print("No tasks.")

while True:
    print("\nOptions:")
    print("1. Add Task")
    print("2. Delete Task")
    print("3. View Tasks")
    print("4. Exit")
    choice = input("Enter your choice (1-4): ")

    if choice == '1':
        add_task()
    elif choice == '2':
        delete_task()
    elif choice == '3':
        view_tasks()
    elif choice == '4':
        print("Exiting program.")
        break
    else:
        print("Invalid choice. Please enter a number from 1 to 4.")
