# Assignment: The Smart Number Parrot & Fraction Splitter

## Problem Statement

In this assignment, you will build an interactive command-line Python program featuring a persistent menu.

The program will:

* Accept numbers from the user.
* Distinguish between integers and floating-point numbers.
* Handle invalid inputs gracefully using exception handling.
* Process decimal values and represent their fractional portions as mathematical fractions.
* Continue displaying the menu until the user explicitly chooses to exit.

---

# Core Requirements

## 1. Interactive Menu Loop

The program must display a continuous menu with two options:

* **`1`**: Give a fraction/number
* **`2`**: Exit

```text
=== NUMBER PARROT MENU ===
1. Give a fraction/number
2. Exit
Enter your choice (1 or 2):
```

The menu must continue to appear after each operation until the user chooses option `2`.

---

## 2. Input & Exception Handling

When option `1` is selected, user should to asked for a number through keyboard.

Invalid input such as `apple` or `hello` must:

* Be handled appropriately.
* Display an appropriate error message.
* Not crash the program.
* Pause for **Enter**.
* Return safely to the main menu.

```text
Error: That is not a valid number! Please try again.
```

---

## 3. Integer Handling — "The Parrot"

If the user enters a valid integer, such as `42` or `-7`, the program must echo it back with a parrot-style message.

```text
Squawk! You have made me a parrot. I am just going to print whatever you have given: 42
```

The integer should be displayed as the value provided by the user.

---

## 4. Float Handling — Whole Number & Fraction Split

If the user enters a floating-point number, separate it into:

1. The whole-number part.
2. The fractional (decimal) part.

The fractional portion must be converted into a mathematical fraction.

Examples:

```text
3.5 → 3 and 1/2
0.5 → 1/2
```

---

## 5. Pause for Key Press

After displaying a result or error, the program must pause and wait for the user to press **Enter** before returning to the main menu.

---

# Example Program Flow

A possible interaction with the program:

```text
=== NUMBER PARROT MENU ===
1. Give a fraction/number
2. Exit
Enter your choice (1 or 2): 1

Enter a number: 3.5
Result: 3 and 1/2

Press Enter to continue...

=== NUMBER PARROT MENU ===
1. Give a fraction/number
2. Exit
Enter your choice (1 or 2): 1

Enter a number: apple
Error: That is not a valid number! Please try again.

Press Enter to continue...

=== NUMBER PARROT MENU ===
1. Give a fraction/number
2. Exit
Enter your choice (1 or 2): 1

Enter a number: 10
Squawk! I have made me a parrot. I am just going to print whatever you have given: 10

Press Enter to continue...

=== NUMBER PARROT MENU ===
1. Give a fraction/number
2. Exit
Enter your choice (1 or 2): 2

Exiting program. Goodbye!
```
