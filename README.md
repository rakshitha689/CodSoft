tasks = []

while True:
    print("\n1. Add Task")
    print("2. View Tasks")
    print("3. Remove Task")
    print("4. Exit")

    choice = input("Enter your choice: ")

    if choice == "1":
        task = input("Enter a new task: ")
        tasks.append(task)
        print("Task added!")

    elif choice == "2":
        print("\nYour Tasks:")
        for i, task in enumerate(tasks, 1):
            print(i, task)

    elif choice == "3":
        task_no = int(input("Enter task number to remove: "))
        if 0 < task_no <= len(tasks):
            tasks.pop(task_no-1)
            print("Task removed!")
        else:
            print("Invalid task number")

    elif choice == "4":
        break

    else:
        print("Invalid choice")
