# To-Do-List

tasks = []

def add_task():
    task = input("Enter a new task: ")
    tasks.append(task)
    print("Task added successfully")

def remove_task():
    task = input("Enter the task to remove: ")
    if task in tasks:
        tasks.remove(task)
        print("Task removed successfully")
    else:
        print("Task not found")

def view_tasks():
    if tasks:
        print("Your tasks:")
        for index, task in enumerate(tasks):
            print(f"{index + 1}. {task}")
    else:
        print("No tasks found")

def main():
    while True:
        print("\nMenu:")
        print("1. Add task")
        print("2. Remove task")
        print("3. View tasks")
        print("4. Quit")

        choice = input("Enter your choice: ")

        if choice == "1":
            add_task()
        elif choice == "2":
            remove_task()
        elif choice == "3":
            view_tasks()
        elif choice == "4":
            break
        else:
            print("Invalid choice")

if __name__ == "__main__":
    main()
