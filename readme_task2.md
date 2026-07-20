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
