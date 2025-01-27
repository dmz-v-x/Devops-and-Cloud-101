# Introduction to Bash Scripting

## Table of Contents
- [Introduction to Bash Scripting](#introduction-to-bash-scripting)
  - [Table of Contents](#table-of-contents)
  - [What is Bash Scripting?](#what-is-bash-scripting)
  - [When to Use Bash Scripting?](#when-to-use-bash-scripting)
  - [Why Use Bash Scripting?](#why-use-bash-scripting)
  - [How to Use Bash Scripting](#how-to-use-bash-scripting)
    - [Step 1: Create a Bash Script](#step-1-create-a-bash-script)
    - [Step 2: Make the Script Executable](#step-2-make-the-script-executable)
    - [Step 3: Run the Script](#step-3-run-the-script)
  - [Advantages of Bash Scripting](#advantages-of-bash-scripting)
  - [Real-World Example](#real-world-example)
  - [Introductory Parts of Bash Scripting](#introductory-parts-of-bash-scripting)
  - [Using Vim for Bash Scripting](#using-vim-for-bash-scripting)
    - [Step 1: Open/Create a File](#step-1-opencreate-a-file)
    - [Step 2: Basic Vim Commands](#step-2-basic-vim-commands)
    - [Step 3: Advanced Vim Features](#step-3-advanced-vim-features)
  - [Advanced Topics](#advanced-topics)
  - [Conclusion](#conclusion)

---

## What is Bash Scripting?
**Bash** (Bourne Again SHell) is a command-line shell and scripting language used to interact with Unix-based operating systems (Linux, macOS). **Bash scripting** involves writing a series of commands in a file (script) to automate tasks, execute programs, or manage system operations.

---

## When to Use Bash Scripting?
Bash scripting is useful in the following scenarios:
- **Automating repetitive tasks** (e.g., backups, log cleanup).
- **Combining multiple commands** into a single script.
- **System administration** (user management, installations).
- **File manipulation** (creating, deleting, renaming files in bulk).
- **Running scheduled tasks** via `cron` jobs.

---

## Why Use Bash Scripting?
- **Simplicity**: Easy to learn for beginners.
- **Ubiquity**: Pre-installed on most Unix-based systems.
- **Speed**: Quick to write and execute for small tasks.
- **Flexibility**: Integrates with CLI tools like `grep`, `awk`, `sed`.

---

## How to Use Bash Scripting

### Step 1: Create a Bash Script
1. Open a text editor (e.g., Vim, Nano).
2. Start the script with a **shebang line**:
   ```bash
   #!/bin/bash
   ```
3. Add your commands:
   ```bash
    echo "Hello World!"
   ```

### Step 2: Make the Script Executable
    ```bash
    chmod +x script_name.sh
    ```

### Step 3: Run the Script
    ```bash
    ./script_name.sh
    ```

---

## Advantages of Bash Scripting
**Portability**: Works across Unix-based systems.

**Automation**: Reduces manual intervention.

**Integration**: Combines CLI tools seamlessly.

**Lightweight**: No compilation required.

---

## Real-World Example
**Backup Script**: Automate daily backups of a directory.

```bash
#!/bin/bash
# Backup script
backup_dir="/home/user/documents"
dest_dir="/home/user/backups"

tar -czf "${dest_dir}/backup_$(date +%Y%m%d).tar.gz" "$backup_dir"
echo "Backup completed on $(date)"
```
---

## Introductory Parts of Bash Scripting

**1. Variables**
  - Store data for reuse.

    ```bash
    name="Alice"
    echo "Hello, $name"
    ```

**2. Command Substitution**
  - Capture command output.

    ```bash
    current_date=$(date)
    echo "Today is $current_date"
    ```

**3. Control Structures**
  - If-Else:

    ```bash
    if [ -f "file.txt" ]; then
    echo "File exists."
    else
    echo "File not found."
    fi
    ```
  - Loops:

    ```bash
    for i in {1..5}; do
    echo "Count: $i"
    done
    ```

**4. Functions**
  - Reusable code blocks.

    ```bash
    greet() {
      echo "Welcome, $1!"
    }
    greet "Bob"
    ```

**5. Input/Output**

  - Read user input:

    ```bash
    read -p "Enter your name: " username
    echo "Hello, $username"
    ```

**6. Exit Status**
  - Check if a command succeeded:

    ```bash
    if grep "error" logfile.txt; then
      echo "Errors found!"
    fi
    ```
---

## Using Vim for Bash Scripting

### Step 1: Open/Create a File

  ```bash
  vim script_name.sh
  ```

### Step 2: Basic Vim Commands

- **Insert Mode:** Press i to start typing.

- **Save and Exit:**

  - Press `Esc` to exit insert mode.
  - Type `:wq` and press Enter.

- **Discard Changes:** `:q!`.

### Step 3: Advanced Vim Features

- **Syntax Highlighting:** Add syntax on to ~/.vimrc.

- **Line Numbers:** Type :set number.

- **Search:** Press / and type your query.

- **Replace:** :%s/old/new/g.

## Advanced Topics

**1. Debugging**
Run a script in debug mode:

```bash
bash -x script_name.sh
```

**2. Error Handling**
Exit on error:

```bash
set -e
```

**3. Traps**
Handle signals (e.g., Ctrl+C):

```bash
trap "echo 'Script interrupted'; exit" SIGINT
```

**4. Using awk and sed**
Process text efficiently:

```bash
awk '{print $1}' file.txt  # Print first column
sed 's/old/new/g' file.txt # Replace text
```

## Conclusion
Bash scripting is a powerful tool for automating tasks, managing systems, and improving productivity. Start with simple scripts, practice regularly, and explore advanced features as you grow comfortable. Use Vim or your favorite editor to write scripts, and remember: the best way to learn is by doing!