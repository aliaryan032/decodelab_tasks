# DecodeLabs Project 1: The To-Do List

## Overview
This repository contains the solution for Task 1 of the DecodeLabs Industrial Training Kit. The project is a Python-based command-line application that functions as a To-Do List. It demonstrates fundamental Data Management concepts, representing the "Logic Skeleton" of backend engineering by storing data in memory using lists and dictionaries.

## Features
* **Add Tasks:** Users can input new tasks, which are actively stored in memory and assigned a unique ID.
* **View Tasks:** The program uses iteration to display the current state of the database, showing all stored tasks.
* **Interactive Menu:** A continuous loop keeps the application running until the user explicitly chooses to terminate the process.

## Execution Output
The application successfully processes input, modifies data, and outputs the display. Below is a demonstration of the program in action:

```text
=== WELCOME TO THE DECODELABS TO-DO SYSTEM ===

--- MENU ---
1. Add a New Task
2. View All Tasks
3. Exit Program
Select an option (1-3): 1
Enter the task description: fill the bottel
Success! Added task ID 1: 'fill the bottel'

--- MENU ---
1. Add a New Task
2. View All Tasks
3. Exit Program
Select an option (1-3): 2

--- YOUR TO-DO LIST ---
1. [ID: 1] -> fill the bottel

--- MENU ---
1. Add a New Task
2. View All Tasks
3. Exit Program
Select an option (1-3): 3
Thank you for using the DecodeLabs system. Goodbye!
------------------------------------------------------------------------------------------------------------------------------
# DecodeLabs Project 2: The Expense Tracker

## Overview
This repository contains the solution for Project 2 of the DecodeLabs Industrial Training Kit[cite: 2]. This project represents the processing phase of backend engineering, focusing specifically on Data Accumulation[cite: 2]. The application is a command-line script that processes continuous numerical data entry, storing, updating, and calculating a running total in real-time[cite: 2].

## Architecture & Features
* **State Preservation:** The `total` variable is safely initialized outside the loop to maintain the state (memory) without being overwritten[cite: 2].
* **Continuous Audit Loop:** Utilizes a `while True:` loop to handle a continuous stream of transaction inputs[cite: 2].
* **Defensive Coding (Poka-Yoke):** Implements a `try...except ValueError` block to act as an error-proofing shield[cite: 2]. It catches invalid string inputs (e.g., text instead of numbers) and prevents the application from crashing[cite: 2].
* **Accumulator Pattern:** Processes valid integers by adding them to the ongoing ledger (`total += new_expense`)[cite: 2].
* **The Kill Switch (Sentinel Value):** Allows the user to gracefully shut down the loop by entering the sentinel value `'quit'`[cite: 2], which immediately breaks the loop and outputs the final mathematical truth[cite: 2].

## Execution Output
The application successfully receives raw data, validates it, transforms it, and accumulates the total. Below is a demonstration of the program in action, including handling invalid data:

```text
=== DECODELABS EXPENSE TRACKER ===
Type 'quit' at any time to stop the machine and see your final bill.

Enter an expense amount: 100
--> Accepted! Current total is: $100

Enter an expense amount: 50
--> Accepted! Current total is: $150

Enter an expense amount: ten
--> Invalid Data! Please enter a valid number.

Enter an expense amount: 20
--> Accepted! Current total is: $170

Enter an expense amount: quit

-------------------------
FINAL TOTAL SPENT: $170
-------------------------
------------------------------------------------------------------------------------------------------------------------------

Author
M. Aryan Ali
