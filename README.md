# Exception Handling in C++

**Aim:**
To study and implement the concept of **Exception Handling** in C++.

**Tools Used:**
VS Code or Online C++ Compiler

---

## Theory

In C++, **Exception Handling** is a mechanism that allows a program to handle unexpected situations (errors) without crashing. Instead of stopping execution when an error occurs, the program can **“catch” the error, process it gracefully, and continue running**.

Errors like division by zero, invalid inputs, or insufficient balance in a banking system can be managed using exceptions.

### Exception Handling Keywords in C++

* **`try` block:**
  Contains the code that might generate an exception (error).

* **`throw` statement:**
  Used to signal (or throw) an exception when an error condition is met.

* **`catch` block:**
  Used to handle the exception thrown. Different types of exceptions can have different catch blocks.

### General Syntax

```cpp
try {
    // code that might cause an error
    if (error_condition) {
        throw value; // throwing an exception
    }
}
catch (datatype var) {
    // code to handle the exception
}
```

### Flow of Exception Handling

1. Code inside the `try` block is executed.
2. If an error condition occurs, the `throw` statement is executed.
3. The `catch` block receives the thrown exception and executes its handling code.
4. Program execution continues after the `catch` block, avoiding crashes.

### Why Exception Handling is Important

* Prevents program termination during runtime errors.
* Helps in **graceful error handling** (user-friendly messages).
* Separates **error-handling code** from normal logic.
* Makes programs more **robust and reliable**.

---

## Program 1 – Division by Zero

**Algorithm:**

1. Start the program.
2. Declare two numbers `a` and `b`.
3. Ask the user to input both numbers.
4. Inside a `try` block:

   * If denominator `b == 0`, throw an exception.
   * Otherwise, perform division `a / b` and print the result.
5. Inside the `catch` block:

   * Print a message saying “Denominator cannot be zero.”
6. Stop the program.

---

## Program 2 – ATM Transaction System

**Algorithm:**

1. Start the program.
2. Define a class `ATM` with:

   * `balance` as private data member.
   * Member functions:

     * `deposit(amount)` → throws exception if amount ≤ 0.
     * `withdraw(amount)` → throws exception if amount ≤ 0 or amount > balance.
     * `checkBalance()` → displays current balance.
3. In `main()`:

   * Initialize ATM with a default balance (e.g., 5000).
   * Display menu:

     1. Check Balance
     2. Deposit Money
     3. Withdraw Money
     4. Exit
4. Based on user choice:

   * Call appropriate ATM function inside a `try` block.
   * If invalid input or error occurs, handle using `catch`.
5. Continue until user selects Exit.
6. Stop the program.

---

## Program 3 – Age Validation

**Algorithm:**

1. Start the program.
2. Declare a variable `age`.
3. Ask the user to enter age.
4. Inside the `try` block:

   * If `age < 0`, throw age (invalid input).
   * Else if `age < 18`, throw age (below 18 case).
   * Else, print “Accepted”.
5. Inside the `catch` block:

   * If age < 0, display “Invalid age”.
   * Else, display “You are below 18”.
6. Stop the program.

---

## Key Learning Outcomes

* Understanding the use of **try, throw, and catch** in C++.
* Ability to handle errors like division by zero, invalid user input, or insufficient balance.
* Importance of separating **normal logic from error-handling logic**.
* Writing programs that are **robust, secure, and user-friendly**.

---

## Applications

* **Banking Systems:** Preventing invalid withdrawals, deposits, and account errors.
* **Data Entry Systems:** Validating user inputs like age, salary, ID numbers.
* **Mathematical Operations:** Avoiding crashes from division by zero or invalid calculations.
* **File Handling:** Handling missing or corrupted files.
* **Networking:** Managing connectivity failures and timeouts gracefully.

---

## Advantages of Exception Handling

* Prevents abnormal termination of programs.
* Provides **clear error messages** to users.
* Improves **program reliability and robustness**.
* Allows **centralized error handling** instead of scattering it everywhere.
* Makes debugging and maintenance easier.
