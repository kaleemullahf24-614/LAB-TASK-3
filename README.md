# LAB-TASK-3:
# TASK NO 1:
List Operations
# Define two lists
list1 = [1, 2, 3]
list2 = [4, 5, 6]
# 1. Combine lists
combined = list1 + list2
print("Combined List:", combined)
# 2. Repeat elements
repeated = list1 * 3
print("Repeated List:", repeated)
# 3. Check membership
print("2 in list1:", 2 in list1)  # True
print("7 not in list2:", 7 not in list2)  # True
# OUTPUT:
Combined List: [1, 2, 3, 4, 5, 6]
Repeated List: [1, 2, 3, 1, 2, 3, 1, 2, 3]
2 in list1: True
7 not in list2: True

# TASK NO 2:
# List Operations:
# Define a list
numbers = [1, 2, 3]
# 1. Append and extend
numbers.append(4)
numbers.extend([5, 6])
print("Appended and Extended List:", numbers)
# 2. Insert, remove, and pop
numbers.insert(2, 99)  # Insert 99 at index 2
print("List after insertion:", numbers)
numbers.remove(99)  # Remove first occurrence
print("List after removal:", numbers)
last_item = numbers.pop()  # Remove last item
print("Last item popped:", last_item)
print("List after popping:", numbers)
# Output:
Appended and Extended List: [1, 2, 3, 4, 5, 6]
List after insertion: [1, 2, 99, 3, 4, 5, 6]
List after removal: [1, 2, 3, 4, 5, 6]
Last item popped: 6
List after popping: [1, 2, 3, 4, 5]

# TASK NO 3:
# Loop Iterations:
# Define a list
fruits = ["apple", "banana", "cherry"]
# 1. For loop iteration
print("For Loop Iteration:")
for fruit in fruits:
    print(fruit)
# 2. While loop iteration
print("\nWhile Loop Iteration:")
i = 0
while i < len(fruits):
    print(fruits[i])
    i += 1
# 3. Using enumerate for index tracking
print("\nUsing Enumerate for Index Tracking:")
for index, fruit in enumerate(fruits):
    print(index, fruit)
# Output:
# For Loop Iteration:
apple
banana
cherry
# While Loop Iteration:
apple
banana
cherry
# Using Enumerate for Index Tracking:
0 apple
1 banana
2 cherry

# TASK NO 4:
# List Comprehensions:
# 1. Basic list comprehension
print("Basic List Comprehension:")
squares = [x**2 for x in range(10)]
print(squares)
# 2. Conditional list comprehension
print("\nConditional List Comprehension:")
even_numbers = [x for x in range(10) if x % 2 == 0]
print(even_numbers)
# 3. Nested list comprehensions
print("\nNested List Comprehensions:")
matrix = [[i * j for j in range(3)] for i in range(3)]
for row in matrix:
    print(row)
# Output:
# Basic List Comprehension:
[0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
# Conditional List Comprehension:
[0, 2, 4, 6, 8]
# Nested List Comprehensions:
[0, 0, 0]
[0, 1, 2]
[0, 2, 4]

# TASK NO 5:
Deque Operations and List Iteration
from collections import deque
# Deque operations
print("Deque Operations:")
d = deque([1, 2, 3])
d.appendleft(0)
print(d)
# Avoid modifying lists during iteration
print("\nAvoid Modifying Lists During Iteration:")
numbers = [1, 2, 3, 4, 5]
numbers = [x for x in numbers if x % 2 == 0]  # Remove odd numbers
print(numbers)
# Output:
# Deque Operations:
deque([0, 1, 2, 3])
# Avoid Modifying Lists During Iteration:
[2, 4]
# TASK NO 6:
# Statistics and To-Do List Manager
# Statistics
print("Statistics:")
marks = [88, 76, 90, 85, 72]
highest = max(marks)
lowest = min(marks)
average = sum(marks) / len(marks)
print(f"Highest: {highest}, Lowest: {lowest}, Average: {average:.2f}")
# To-Do List Manager
print("\nTo-Do List Manager:")
tasks = []
# while True:
    print("Options:")
    print("1. Add task")
    print("2. Remove task")
    print("3. Display tasks")
    print("4. Quit")
    choice = input("Choose an option: ")
    if choice == "1":
        task = input("Enter a task: ")
        tasks.append(task)
        print("Task added!")
    elif choice == "2":
        task = input("Enter a task to remove: ")
        if task in tasks:
            tasks.remove(task)
            print("Task removed!")
        else:
            print("Task not found!")
    elif choice == "3":
        print("Tasks:")
        for i, task in enumerate(tasks, start=1):
            print(f"{i}. {task}")
    elif choice == "4":
        print("Goodbye!")
        break
    else:
        print("Invalid option. Please choose again.")




