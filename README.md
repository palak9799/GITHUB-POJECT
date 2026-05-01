# GITHUB-POJECT
students = []

while True:
    print("\n--- Student Management System ---")
    print("1. Add Student")
    print("2. View Students")
    print("3. Search Student")
    print("4. Exit")

    choice = input("Enter your choice: ")

    if choice == '1':
        name = input("Enter student name: ")
        marks = int(input("Enter marks: "))
        students.append({"name": name, "marks": marks})
        print("Student added successfully!")

    elif choice == '2':
        if len(students) == 0:
            print("No students found.")
        else:
            print("\nStudent List:")
            for s in students:
                print("Name:", s["name"], "| Marks:", s["marks"])

    elif choice == '3':
        search_name = input("Enter name to search: ")
        found = False
        for s in students:
            if s["name"].lower() == search_name.lower():
                print("Student Found:", s)
                found = True
                break
        if not found:
            print("Student not found.")

    elif choice == '4':
        print("Exiting program...")
        break

    else:
        print("Invalid choice. Try again.")
