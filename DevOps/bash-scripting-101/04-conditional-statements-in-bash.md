# Comprehensive Guide to Conditional Statements in Linux Shell Scripting

## Table of Contents
- [Comprehensive Guide to Conditional Statements in Linux Shell Scripting](#comprehensive-guide-to-conditional-statements-in-linux-shell-scripting)
  - [Table of Contents](#table-of-contents)
  - [Introduction to Conditional Statements](#introduction-to-conditional-statements)
  - [Basic Syntax of Conditional Statements](#basic-syntax-of-conditional-statements)
    - [The `if` Statement](#the-if-statement)
    - [The `if-else` Statement](#the-if-else-statement)
    - [The `elif` Statement](#the-elif-statement)
  - [Advanced Conditional Statements](#advanced-conditional-statements)
    - [Logical Operators](#logical-operators)
    - [Nested Conditionals](#nested-conditionals)
    - [Case Statements](#case-statements)
  - [Best Practices for Using Conditionals](#best-practices-for-using-conditionals)
  - [Practical Examples](#practical-examples)
    - [Example 1: File Backup Script](#example-1-file-backup-script)
    - [Example 2: User Input Validation](#example-2-user-input-validation)
    - [Example 3: System Monitoring](#example-3-system-monitoring)
  - [Conclusion](#conclusion)

---

## Introduction to Conditional Statements

Conditional statements are fundamental to programming and scripting. They allow your scripts to make decisions based on specific conditions. In Linux shell scripting, conditionals are primarily implemented using `if`, `elif`, `else`, and `case` statements. This guide will cover everything from basic syntax to advanced usage.

---

## Basic Syntax of Conditional Statements

### The `if` Statement
The simplest form of a conditional statement checks if a condition is true and executes a block of code accordingly.

Syntax:

    if [ condition ]; then
        # Code to execute if condition is true
    fi

Example:

    # Check if a file exists
    if [ -f "/path/to/file.txt" ]; then
        echo "File exists."
    fi

### The `if-else` Statement
The `if-else` statement adds an alternative path if the condition is false.

Syntax:

    if [ condition ]; then
        # Code if condition is true
    else
        # Code if condition is false
    fi

Example:

    # Check if a user is root
    if [ "$(whoami)" = "root" ]; then
        echo "You are root."
    else
        echo "You are not root."
    fi

### The `elif` Statement
Use `elif` to test multiple conditions sequentially.

Syntax:

    if [ condition1 ]; then
        # Code if condition1 is true
    elif [ condition2 ]; then
        # Code if condition2 is true
    else
        # Code if all conditions are false
    fi

Example:

    # Grade classification
    read -p "Enter your score: " score
    if [ $score -ge 90 ]; then
        echo "Grade A"
    elif [ $score -ge 80 ]; then
        echo "Grade B"
    else
        echo "Grade C"
    fi

---

## Advanced Conditional Statements

### Logical Operators
Combine conditions using logical operators:
- **AND (`&&`)** or `-a`
- **OR (`||`)** or `-o`
- **NOT (`!`)**

Example with `&&`:

    # Check if a file exists and is readable
    if [ -f "/path/to/file.txt" ] && [ -r "/path/to/file.txt" ]; then
        echo "File exists and is readable."
    fi

Example with `-o`:

    # Check if the number is 10 or 20
    if [ $num -eq 10 -o $num -eq 20 ]; then
        echo "Number is 10 or 20."
    fi

### Nested Conditionals
Conditionals can be nested within each other for complex logic.

Example:

    # Check if a user is an admin and has write access
    if [ "$role" = "admin" ]; then
        if [ -w "/var/log" ]; then
            echo "Admin has write access."
        fi
    fi

### Case Statements
The `case` statement simplifies multi-condition checks by matching patterns.

Syntax:

    case "$variable" in
        pattern1)
            # Code for pattern1
            ;;
        pattern2)
            # Code for pattern2
            ;;
        *)
            # Default case
            ;;
    esac

Example:

    # Handle user input
    read -p "Enter yes/no: " choice
    case "$choice" in
        [Yy]es)
            echo "You agreed."
            ;;
        [Nn]o)
            echo "You disagreed."
            ;;
        *)
            echo "Invalid input."
            ;;
    esac

---

## Best Practices for Using Conditionals

1. **Use Double Brackets for Advanced Tests**
   Prefer `[[ ]]` over `[ ]` for string comparisons and regex matching.
   Example:

        if [[ "$str" == *"linux"* ]]; then
            echo "String contains 'linux'."
        fi

2. **Quote Variables to Prevent Errors**
   Always quote variables to handle spaces or special characters.
   Example:

        if [ "$var" = "value" ]; then

3. **Use Indentation for Readability**
   Indent code blocks to improve readability.

4. **Check Command Success**
   Use `$?` to check the exit status of a command.
   Example:

        grep "error" /var/log/syslog
        if [ $? -eq 0 ]; then
            echo "Errors found in syslog."
        fi

---

## Practical Examples

### Example 1: File Backup Script

    #!/bin/bash
    backup_dir="/backup"
    if [ ! -d "$backup_dir" ]; then
        mkdir -p "$backup_dir"
        echo "Backup directory created."
    else
        echo "Backup directory already exists."
    fi

### Example 2: User Input Validation

    #!/bin/bash
    read -p "Enter a number (1-5): " num
    if [[ "$num" =~ ^[1-5]$ ]]; then
        echo "Valid number."
    else
        echo "Invalid number."
    fi

### Example 3: System Monitoring

    #!/bin/bash
    cpu_load=$(uptime | awk '{print $10}')
    if (( $(echo "$cpu_load > 5.0" | bc -l) )); then
        echo "High CPU load detected: $cpu_load"
    else
        echo "CPU load is normal."
    fi

---

## Conclusion

Conditional statements are the backbone of decision-making in shell scripting. From basic `if-else` checks to advanced `case` statements, mastering these constructs will enable you to write robust and efficient scripts. Practice with real-world examples and adhere to best practices to avoid common pitfalls.
