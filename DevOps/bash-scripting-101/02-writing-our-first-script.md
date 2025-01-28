# Bash Scripting Fundamentals

## Table of Contents
1. [Difference Between Bash and Shell](#difference-between-bash-and-shell)
2. [What is a Shebang?](#what-is-a-shebang)
3. [How to Create a Bash Script File](#how-to-create-a-bash-script-file)
4. [How to Execute a Bash Script File](#how-to-execute-a-bash-script-file)
5. [How to Comment in a Bash Script](#how-to-comment-in-a-bash-script)
6. [How to Declare Variables in Bash Scripts](#how-to-declare-variables-in-bash-scripts)
7. [Different Types of Quotes in Bash Scripts
](#different-types-of-quotes-in-bash-scripts)
8. [Command Line Arguments in Bash Scripts](#command-line-arguments-in-bash-scripts)
9. [Environment Variables in Bash](#environment-variables-in-bash)

---

## Difference Between Bash and Shell

### 1. **Definition**:
   - **Shell**: A shell is a command-line interface (CLI) that allows users to interact with the operating system by typing commands. It acts as an intermediary between the user and the kernel. There are many types of shells, such as **Bash**, **Zsh**, **Fish**, **Ksh**, etc.
   - **Bash**: **Bash** (Bourne Again Shell) is a specific type of shell. It is an enhanced version of the Bourne Shell (`sh`), with additional features and improvements. Bash is the default shell in many Linux distributions and macOS (prior to macOS Catalina).

### 2. **Usage**:
   - **Shell**: Refers to any command-line interface that interprets and executes commands (could be Bash, Zsh, Fish, etc.).
   - **Bash**: A specific shell that provides powerful scripting capabilities and is widely used in Linux/Unix systems.

### 3. **Features**:
   - **Shell**: Each shell has its own unique features, built-in commands, syntax, and behavior.
   - **Bash**: Bash includes features like command history, command completion, variables, and functions, which are more user-friendly and powerful than older shells like the Bourne Shell (`sh`).

### 4. **Scripting**:
   - **Shell**: Any shell can be used to write scripts, but the syntax and capabilities differ across different types of shells.
   - **Bash**: Bash scripts are often written using Bash syntax, which is specifically designed to make scripting more efficient and easier.

### 5. **Portability**:
   - **Shell**: Scripts written in different shells might not be portable across systems if they rely on shell-specific features.
   - **Bash**: Bash scripts are highly portable across Unix-like systems (Linux, macOS) where Bash is installed.

### 6. **Compatibility**:
   - **Shell**: Different shells may have different commands and functionality, leading to incompatibility in terms of syntax or behavior.
   - **Bash**: While compatible with many traditional Unix commands, Bash has its own set of commands and syntax, making it different from other shells.

### Conclusion:
- **Shell** is a generic term for command-line interpreters, while **Bash** is a specific, popular shell.
- Bash is one of the most widely used shells, known for its rich features and scripting capabilities.

---

## What is a Shebang?

- A **shebang** is the first line in a script file that tells the system which interpreter to use to execute the script.
- It is written as `#!` followed by the path to the interpreter (e.g., `/bin/bash`, `/usr/bin/python3`).

    ### Example:
    ```bash
    #!/bin/bash
    ```
- The shebang is commonly used in shell scripts and programming scripts like Python, Perl, Ruby, etc.
- When the script is executed, the system uses the interpreter specified in the shebang to run the file, even if the user does not explicitly call the interpreter.

### Common Shebang Examples:

- For a Bash script:
  `#!/bin/bash`

- For a Python script:
  `#!/usr/bin/python3`

- For a Perl script:
  `#!/usr/bin/perl`

### Why Use a Shebang?

- **Portability**: It ensures that the script can be run on different systems, as it automatically invokes the appropriate interpreter.

- **Convenience**: You don’t need to explicitly specify the interpreter every time you run the script.

### How it Works:
1. When you execute a script with a shebang, the system uses the shebang line to determine which interpreter should run the script.
2. The operating system then looks up the interpreter in the specified path and runs the script using that interpreter.

---

## How to Create a Bash Script File

To create a bash script file, follow these steps:

### 1. Open a terminal
First, open your terminal on a Linux or macOS machine.

### 2. Create a new file
You can create a new file using a text editor like `nano`, `vim`, or any other editor of your choice.

For example, to create a file called `myscript.sh` using `nano`, run:
```bash
nano myscript.sh
```

### 3. Add the shebang line
At the very top of the file, add the shebang line to specify the interpreter:

```bash
#!/bin/bash
```

### 4. Write the script
After the shebang line, add the bash commands you want the script to execute. For example:

```bash
#!/bin/bash
echo "Hello, World!"
```

### 5. Save and exit

- If you are using nano, press CTRL + X to exit, then press Y to save the changes, followed by Enter to confirm the file name.
- If you're using vim, press Esc, then type :wq and press Enter to save and quit.

### 6. Make the script executable
Before running the script, you need to make it executable. In the terminal, use the chmod command:

```bash
chmod +x myscript.sh
```

### 7. Run the script
Now, you can run your script by typing:

```bash
./myscript.sh
```

### Summary of Steps:
1. Open a terminal.
2. Create the script file using a text editor (nano myscript.sh).
3. Add the shebang line (#!/bin/bash).
4. Write your bash commands.
5. Save and exit the editor.
6. Make the script executable (chmod +x myscript.sh).
7. Run the script (./myscript.sh).
8. Copy code

---

## How to Execute a Bash Script File

After creating your Bash script file, you need to execute it. Here's how you can do it:

### 1. Make Sure the Script is Executable
Before running the script, ensure that it has executable permissions. You can do this with the `chmod` command:

```bash
chmod +x myscript.sh
```

This gives the script execute permissions, allowing you to run it directly.

### 2. Execute the Script from the Terminal
To execute the script, there are a few different methods:

**Method 1: Using ./ (Recommended)**
This method allows you to run the script directly from the directory where it's located:

```bash
./myscript.sh
```

The ./ tells the system to execute the script from the current directory.

**Method 2: Using the Absolute Path**
If the script is located in a different directory, you can provide the absolute path to the script:

```bash
/path/to/script/myscript.sh
```

For example, if your script is in /home/user/scripts, you would run:

```bash
/home/user/scripts/myscript.sh
```

**Method 3: Using the Shell Command**
You can also run the script using a shell explicitly, like bash:

```bash
bash myscript.sh
```

This method works even if the script is not executable (but you still need to provide the correct path).

**Method 4: Running via sh**
If you are using sh or any other shell (like zsh), you can run the script by calling that shell:

```bash
sh myscript.sh
```

### Additional Notes:
- Running without chmod +x: If you don't want to change the file permissions with chmod, you can always run the script using bash myscript.sh or sh myscript.sh (as shown above).

- Scripts in $PATH: If your script is in a directory listed in your system's $PATH variable, you can execute it from anywhere by just typing its name (no need for ./ or full path).

## Example of Execution:
Let's say you created a script called myscript.sh with the following contents:

```bash
#!/bin/bash
echo "Hello, World!"
```

You can execute it by:

1. **Making it executable:**
    ```bash
    chmod +x myscript.sh
    ```

2. **Running it:**
    ```bash
    ./myscript.sh
    ```

    This will output:

    ```bash
    Hello, World!
    ```
### Summary of Methods to Execute a Bash Script:
1. `./myscript.sh` (Recommended if in the current directory).
2. `/path/to/script/myscript.sh` (Absolute path).
3. `bash myscript.sh` (Explicitly call Bash).
4. `sh myscript.sh` (Using sh).

---

## How to Comment in a Bash Script

In a Bash script, comments are used to add explanations or notes without affecting the script's execution. Here's how you can comment:

### 1. Single-Line Comments

- To comment a single line in a Bash script, use the `#` symbol at the beginning of the line.

```bash
# This is a single-line comment
echo "Hello, World!"  # This is an inline comment
```

Everything after the # on that line is ignored by the Bash interpreter.

### 2. Multi-Line Comments
Bash does not have a built-in syntax for multi-line comments like some other languages, but you can achieve it in two ways:

**Method 1: Using Multiple # for Each Line**
For multi-line comments, simply use # on each line:

```bash
# This is a comment
# that spans multiple
# lines in a Bash script.
```

**Method 2: Using a : <<'COMMENT' Block (Heredoc)**

You can use a heredoc to create a block of comments, although it’s less common. This method redirects a block of text to nowhere (since no command follows the heredoc).

```bash
: <<'COMMENT'
This is a multi-line comment.
Everything between the COMMENT tag will be ignored.
You can use this for large blocks of comments.
COMMENT
```

Note: The text inside the COMMENT block will be treated as a comment and ignored by the script.

**Example of Commenting in a Bash Script**

```bash
#!/bin/bash

# This script prints "Hello, World!" to the terminal

echo "Hello, World!"  # Print message

# This is a simple script with comments
# You can add explanations like this.

: <<'MULTI_LINE_COMMENT'
This block of text
is ignored by the Bash interpreter
and can be used for large comments.
MULTI_LINE_COMMENT
```

### Summary:
**Single-line comments:** Use # at the start of the line.
**Multi-line comments:** Use # on each line or the : <<'COMMENT' heredoc approach.
By using comments, you can make your Bash scripts more readable and maintainable.

---

## How to Declare Variables in Bash Scripts

In Bash scripts, variables are used to store data that can be referenced and manipulated throughout the script. Here's how to declare and use variables in Bash:

### 1. Declaring Variables

**Basic syntax:** To declare a variable in Bash, simply assign a value to the variable name without any spaces around the `=` sign.

```bash
variable_name=value

Example:

```bash
name="Alice"
```

No spaces: There should be no spaces before or after the = sign when declaring a variable.

```bash
age=25
```

### 2. Accessing Variable Values

- To access or use the value of a variable, prepend the variable name with a $.
Example:

    ```bash
    echo $name    # Output: Alice
    echo $age     # Output: 25
    ```

- In double quotes: It's good practice to enclose variables in double quotes when using them, especially when dealing with spaces or special characters.

    ```bash
    Copy code
    greeting="Hello, $name!"
    echo "$greeting"    # Output: Hello, Alice!
    ```

- Declaring Integer Variables
Variables in Bash can hold integers, and you can perform arithmetic operations on them using (( )) or let.

Example of declaring and performing arithmetic:

```bash
num1=10
num2=5
sum=$((num1 + num2))   # Perform addition
echo $sum              # Output: 15
```

- Declaring Arrays

Bash supports arrays, and you can declare them as follows:

```bash
fruits=("apple" "banana" "cherry")
```

To access array elements:

```bash
echo ${fruits[0]}   # Output: apple
```

- Variable Scope
  - Local Variables: Variables declared within a function are local to that function and are not accessible outside it.
  - Global Variables: Variables declared outside functions are global by default and can be accessed anywhere in the script.
    Example:

    ```bash
    #!/bin/bash

    global_var="I am a global variable"

    function example_func {
        local local_var="I am a local variable"
        echo $local_var
    }

    echo $global_var    # Output: I am a global variable
    example_func       # Output: I am a local variable
    echo $local_var    # Error: local_var: unbound variable
    ```

- Read User Input and Assign to Variables
You can also read user input and assign it to a variable using the read command.

```bash
echo "Enter your name:"
read user_name
echo "Hello, $user_name!"
```

Example of Variable Declaration in a Bash Script

```bash
#!/bin/bash

# Declare variables
name="Bob"
age=30

# Print variables
echo "Name: $name"
echo "Age: $age"

# Arithmetic operation
num1=100
num2=50
result=$((num1 - num2))
echo "Result of subtraction: $result"

# Array declaration and usage
fruits=("apple" "banana" "cherry")
echo "First fruit: ${fruits[0]}"
```

### Summary:

1.  Declaring a variable: variable_name=value (no spaces around =)
2.  Accessing the value of a variable: $variable_name
3. Integer operations: (( )) for arithmetic
4.  Arrays: Use ()
5.  Local and Global variables: local for local variables inside functions
6.  User input: Use read to assign user input to a variable



---

## Different Types of Quotes in Bash Scripts

In Bash, there are three main types of quotes: **single quotes** (`'`), **double quotes** (`"`), and **backticks** (`` ` ``). Each type of quote behaves differently when used in a Bash script.

### 1. Single Quotes (`'`)

- **Single quotes** are used to enclose a string where the content is treated literally.
- Everything inside single quotes is preserved exactly as typed, and no variable expansion or command substitution happens.

Example:
```bash
str='Hello, $USER'
echo $str   # Output: Hello, $USER
```
In this case, $USER is not expanded because the string is inside single quotes.

Key points:

- No variable expansion.
- No command substitution.
- Escape sequences are not interpreted (e.g., \n won't create a new line).

### 2. Double Quotes (")

Double quotes allow for variable expansion and command substitution inside the quoted string.
They are useful when you want to preserve spaces or special characters but still have variables or commands evaluated.

Example:

```bash
name="Alice"
str="Hello, $name!"
echo $str   # Output: Hello, Alice!
```

The $name variable is expanded inside the double quotes.

Key points:

- **Variable expansion:** $variable will be replaced with the variable's value.
- **Command substitution:** $(command) or `command` will run the command and replace it with the output.
- **Escape sequences:** `\n`, `\t`, etc., are interpreted as special characters (e.g., newline, tab).

### 3. Backticks (`) or $(...)
- Backticks (`command`) and $() are used for command substitution, where the output of a command is substituted into the string.
- Backticks are older and can be harder to read, especially for nested commands, so $() is preferred in modern scripts.

    Example with backticks:

    ```bash
    date_str=`date`
    echo $date_str   # Output: current date and time
    ```

    Example with $() (preferred):

    ```bash
    date_str=$(date)
    echo $date_str   # Output: current date and time
    ```

    Key points:
    - The command inside the backticks or $() is executed, and its output is inserted into the string.
    - Backticks are more difficult to nest, while $() is easier to read and supports nesting.
    -
### 4. Escape Character (\)
- The escape character (\) is used to escape special characters, making them be treated literally (even inside quotes).
- You can escape quotes themselves or other special characters, such as newlines or tabs.
    Example:

    ```bash
    str="This is a \"quoted\" word."
    echo $str   # Output: This is a "quoted" word.
    ```

    Here, the \" escapes the double quote to include it in the string.

    Key points:

    - Escape special characters like quotes, newlines, or tabs.
    - Useful for including characters that would otherwise be interpreted by the shell.


### Summary of Key Differences Between Quotes in Bash

| Feature                     | Single Quotes (`'`)               | Double Quotes (`"`)                | Backticks / `$()`                  |
|-----------------------------|-----------------------------------|-----------------------------------|------------------------------------|
| **Variable Expansion**       | No                                | Yes                               | Yes                                |
| **Command Substitution**     | No                                | Yes                               | Yes (using `$(command)` preferred) |
| **Escape Sequences**         | No                                | Yes                               | Not applicable                     |
| **Literal Strings**          | Everything is treated literally   | Spaces and special characters are preserved, but variables and commands are expanded | Executes command and inserts output |
| **Common Use**               | Enclosing fixed text (no variables) | Enclosing text with variables or commands | Inserting the output of a command  |

### Example Usage:

```bash
#!/bin/bash

# Single quotes: No variable expansion
str1='Hello, $USER'
echo $str1  # Output: Hello, $USER

# Double quotes: Variable expansion
str2="Hello, $USER"
echo $str2  # Output: Hello, <user_name>

# Command substitution using $()
current_time=$(date)
echo "Current time: $current_time"  # Output: Current time: <current_time>
```

By using the appropriate quotes, you can control how strings and variables are treated in your Bash scripts.

---

## Command Line Arguments in Bash Scripts

In Bash scripts, **command line arguments** allow you to pass data to the script when executing it. These arguments can be accessed within the script using special variables.

### 1. Basic Command Line Arguments

When you run a Bash script, you can pass arguments to it. These arguments are stored as variables that can be accessed inside the script.

For example, if you run:

```bash
./myscript.sh arg1 arg2 arg3
```
arg1, arg2, and arg3 are command line arguments.

### 2. Accessing Command Line Arguments
The command line arguments are accessed using special variables:

- $0: The name of the script.
- $1, $2, ..., $n: The positional parameters (arguments passed to the script).
- $#: The number of command line arguments passed to the script.
- $@: All the arguments passed to the script (as a list).
- $*: All the arguments passed to the script (as a single string).

    Example:

    ```bash
    #!/bin/bash

    # Accessing command line arguments
    echo "Script name: $0"
    echo "First argument: $1"
    echo "Second argument: $2"
    echo "Number of arguments: $#"
    echo "All arguments (as a list): $@"
    echo "All arguments (as a single string): $*"
    ```

    If you run the script like this:

    ```bash
    ./myscript.sh arg1 arg2 arg3
    ```

    The output will be:

    ```bash
    Script name: ./myscript.sh
    First argument: arg1
    Second argument: arg2
    Number of arguments: 3
    All arguments (as a list): arg1 arg2 arg3
    All arguments (as a single string): arg1 arg2 arg3
    ```

### 3. Handling Arguments in Loops
You can loop through all the arguments using a for loop. This is helpful if you want to process each argument individually.

Example:

```bash
#!/bin/bash

echo "Processing command line arguments..."
for arg in "$@"; do
  echo "Argument: $arg"
done
```

### 4. Example with Conditional Logic
You can also use conditional statements to check the number of arguments and ensure the script is run with the correct parameters.

Example:

```bash
#!/bin/bash

if [ $# -lt 2 ]; then
  echo "Error: Not enough arguments provided."
  echo "Usage: $0 arg1 arg2"
  exit 1
fi

echo "First argument: $1"
echo "Second argument: $2"
```

If you run the script without two arguments:

```bash
./myscript.sh
```

It will output:

```bash
Error: Not enough arguments provided.
Usage: ./myscript.sh arg1 arg2
```

### 5. Default Values for Missing Arguments
You can also set default values for arguments that are not passed.

Example:

```bash
#!/bin/bash

arg1=${1:-"default_value"}  # If $1 is not provided, use "default_value"
echo "First argument: $arg1"
```

### Summary of Special Variables

| Variable | Description |
|----------|-------------|
| `$0`     | The name of the script. |
| `$1`, `$2`, ..., `$n` | The first, second, ..., nth argument passed to the script. |
| `$#`     | The total number of arguments passed to the script. |
| `$@`     | All arguments passed to the script (as a list). |
| `$*`     | All arguments passed to the script (as a single string). |

Example Usage:

```bash
#!/bin/bash

# Simple script to greet the user with their name
if [ $# -lt 1 ]; then
  echo "Please provide your name."
  exit 1
fi

echo "Hello, $1!"
```

Running the script:

```bash
./greet.sh Alice
```

Output:

```bash
Hello, Alice!
```

Command line arguments make Bash scripts flexible and allow them to process input dynamically when executed.

---

## Environment Variables in Bash

**Environment variables** are dynamic values that affect the behavior of processes in a system. They provide important configuration information to programs and scripts running on a system. In Bash, environment variables can store data such as paths, system configurations, and user-specific settings.

### 1. Types of Environment Variables

- **System-Wide Variables:** These are set globally and are available to all users and processes.
- **User-Specific Variables:** These are set for individual users and are available only to processes that the user runs.
- **Shell-Specific Variables:** These are set for individual shell sessions and are not inherited by other processes.

### 2. Common Environment Variables

Here are some of the most commonly used environment variables in Bash:

- `$HOME`: The current user's home directory.
- `$PATH`: A colon-separated list of directories that the shell searches for commands.
- `$USER`: The name of the current user.
- `$SHELL`: The path of the current shell.
- `$PWD`: The current working directory.
- `$EDITOR`: The default text editor.
- `$LANG`: The system locale settings.

### 3. Viewing Environment Variables

To view all environment variables, you can use the `printenv` or `env` command.

```bash
printenv   # Shows all environment variables
```
To view a specific environment variable:

```bash
echo $HOME   # Outputs the home directory path
```

### 4. Setting Environment Variables
You can set environment variables in the shell or in your .bashrc (or .bash_profile for login shells) file to make them persist across sessions.

- Temporary Environment Variable: Set for the current session only.
    ```bash
    export VAR_NAME="value"
    ```
    Example:

    ```bash
    export MY_VAR="Hello, World!"
    ```

- Persistent Environment Variable: Add to the `.bashrc` or `.bash_profile` file for persistence across shell sessions.

    ```bash
    echo 'export MY_VAR="Hello, World!"' >> ~/.bashrc
    source ~/.bashrc   # Apply the changes immediately
    ```

### 5. Unsetting Environment Variables
To remove an environment variable, use the unset command:

```bash
unset VAR_NAME
```

Example:

```bash
unset MY_VAR
```

### 6. Using Environment Variables in Scripts
You can use environment variables in your scripts to customize behavior.

Example script:

```bash
#!/bin/bash

echo "Hello, $USER!"
echo "Your home directory is $HOME"
echo "Current working directory is $PWD"
```

### 7. Local vs Global Variables
- Local Variables: You can create a variable that only exists within the current shell session without affecting the environment. This can be done by not using the export command.

    Example:

    ```bash
    MY_LOCAL_VAR="Local value"
    ```

- Global Variables: Use the export command to make a variable available globally, so that child processes (like scripts or programs) can access it.

    Example:

    ```bash
    export MY_GLOBAL_VAR="Global value"
    ```

**Example of Environment Variables:**
```bash
#!/bin/bash

# Setting environment variables
export MY_PATH="/home/user/myfolder"
export MY_EDITOR="vim"

# Using environment variables in the script
echo "Path is: $MY_PATH"
echo "Default editor is: $MY_EDITOR"
```

Running this script will output:

```bash
Path is: /home/user/myfolder
Default editor is: vim
```
### Summary of Common Environment Variables

| Variable | Description |
|----------|-------------|
| `$HOME`  | The current user's home directory. |
| `$PATH`  | A list of directories to search for commands. |
| `$USER`  | The name of the current user. |
| `$SHELL` | The path of the current shell. |
| `$PWD`   | The current working directory. |
| `$EDITOR`| The default text editor. |
| `$LANG`  | The system locale settings. |


### Key Commands for Environment Variables:
1. printenv: Displays all environment variables.
2. echo $VAR_NAME: Displays the value of a specific environment variable.
3. export VAR_NAME=value: Sets a new environment variable.
4. unset VAR_NAME: Unsets or removes an environment variable.

---



