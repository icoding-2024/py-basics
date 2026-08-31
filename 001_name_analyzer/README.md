# Assignment: The Smart Name Analyzer & Cleaner

## Problem Statement
In this assignment, you will build a Python program that processes a user's input name. Names can often be messy, containing accidental double spaces, special characters, or numbers. Your program needs to clean the name, validate its contents, calculate its "Name Score" based on specific rules, and display the results.

---

## Core Requirements

1. **Input & Welcome:** Prompt the user to enter their full name using the `input()` function.
2. **Character Validation:**
   - The name should ideally contain **only English alphabets** (uppercase and lowercase) and **spaces**.
   - If the name contains any invalid characters (such as numbers like `1`, `2` or special symbols like `@`, `#`, `$`, `!`), the program must flag it by printing a **"Bad Name!"** warning message, but it should still proceed to calculate the score using the rules below.
3. **String Cleaning (Consecutive Spaces):**
   - If the user enters multiple consecutive spaces between words (e.g., `Vikram  Dhanapalan` with two spaces, or `Vikram   Dhanapalan` with three spaces), the program must clean it up by replacing all consecutive spaces with a **single space** in the final cleaned output.
4. **Scoring System:**
   - **English Letters:** Every valid English alphabet (`a-z`, `A-Z`) earns **+1 point**.
   - **Normal Space:** A single space between words is normal and earns **0 points**.
   - **Extra/Consecutive Spaces:** Any extra consecutive spaces penalize the score. For a block of $k$ consecutive spaces, you have $(k - 1)$ extra spaces. Each extra space costs **-1 point** (e.g., 3 spaces together mean 2 extra spaces, resulting in a **-2 penalty**).
   - **Invalid Symbols:** Any non-alphabet, non-space character (like numbers or punctuation) incurs a **-1 penalty** per symbol.

---

## Output Format
Your program should output:
1. The **Actual Length** of the raw input string.
2. The **Cleaned Name** (with consecutive spaces collapsed into a single space).
3. A **"Bad Name!"** notification if invalid symbols are detected.
4. The **Final Calculated Score**.

---

## Test Cases

### Test Case 1: Standard Name (Valid)
- **Raw Input:** `Vikram Dhanapalan`
- **Cleaned Output:** `Vikram Dhanapalan`
- **Validation Status:** Valid Name
- **Score Calculation Breakdown:** 15 letters ($\times 1$) + 1 normal space ($0$) = $15$
- **Final Score:** **15**

### Test Case 2: Name with Double Space (Valid)
- **Raw Input:** `Vikram  Dhanapalan` *(two spaces)*
- **Cleaned Output:** `Vikram Dhanapalan`
- **Validation Status:** Valid Name
- **Score Calculation Breakdown:** 15 letters ($15$) + 1 extra space ($-1$) = $15 - 1$
- **Final Score:** **14**

### Test Case 3: Name with Triple Space (Valid)
- **Raw Input:** `Vikram   Dhanapalan` *(three spaces)*
- **Cleaned Output:** `Vikram Dhanapalan`
- **Validation Status:** Valid Name
- **Score Calculation Breakdown:** 15 letters ($15$) + 2 extra spaces ($-2$) = $15 - 2$
- **Final Score:** **13**

### Test Case 4: Name with Symbols (Invalid)
- **Raw Input:** `John#Doe!`
- **Cleaned Output:** `John#Doe!`
- **Validation Status:** **Bad Name!**
- **Score Calculation Breakdown:** 7 letters ($7$) + 2 invalid symbols ($-2$) = $7 - 2$
- **Final Score:** **5**

### Test Case 5: Multiple Spacing Irregularities (Valid)
- **Raw Input:** `A  B   C` *(double space between A and B, triple space between B and C)*
- **Cleaned Output:** `A B C`
- **Validation Status:** Valid Name
- **Score Calculation Breakdown:** 3 letters ($3$) + (1 extra space + 2 extra spaces = 3 extra spaces total, $-3$) = $3 - 3$
- **Final Score:** **0**

---

## Python Foundation Topics Covered
By completing this assignment, students will practice and reinforce the following fundamental Python concepts:
- **Input/Output Operations:** Using `input()` to capture user data and `print()` to display formatted results.
- **String Methods & Manipulation:**
  - Checking string is strictly from english letters.
  - Replacing or looping through strings to handle consecutive spaces.
- **Conditional Statements:**
  - Validating character constraints.
  - Triggering the "Bad Name!" warning.
- **Loops:**
  - Iterating through characters in a string to count letters, spaces, and symbols individually.
- **Arithmetic & Assignment Operators:**
  - Tracking scores using cumulative addition and subtraction.