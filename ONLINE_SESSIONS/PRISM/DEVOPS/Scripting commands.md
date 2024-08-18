---
created: 2024-08-18T18:08
updated: 2024-08-18T18:09
---


### Basic Bash Commands:

1. **File and Directory Management**:
    
    - `ls`: Lists files and directories.
    - `cd`: Changes the directory.
    - `pwd`: Displays the current working directory.
    - `mkdir`: Creates a new directory.
    - `rmdir`: Removes an empty directory.
    - `touch`: Creates an empty file or updates the timestamp.
    - `rm`: Deletes a file.
    - `cp`: Copies files or directories.
    - `mv`: Moves or renames files or directories.
    - `cat`: Concatenates and displays file content.
    - `less`: Views file content with pagination.
    - `head` / `tail`: Displays the beginning or end of a file.
2. **File Permissions and Ownership**:
    
    - `chmod`: Changes file permissions.
    - `chown`: Changes file ownership.
3. **Text Processing**:
    
    - `echo`: Displays a message or variable content.
    - `grep`: Searches for a pattern in files.
    - `awk`: Text processing and pattern matching.
    - `sed`: Stream editor for editing text in files.
    - `cut`: Cuts sections from each line of files.
4. **File Search**:
    
    - `find`: Searches for files and directories.
    - `locate`: Finds files by name.
5. **System Information**:
    
    - `uname`: Displays system information.
    - `df`: Displays disk space usage.
    - `du`: Shows disk usage of files and directories.
    - `top` / `htop`: Displays system processes and resource usage.
6. **Networking**:
    
    - `ping`: Checks connectivity with another host.
    - `ifconfig`: Displays or configures network interfaces.
    - `curl`: Transfers data from/to a server.
7. **Compression and Archiving**:
    
    - `tar`: Creates and extracts archive files.
    - `gzip`: Compresses files.
8. **Package Management**:
    
    - `apt` (Debian/Ubuntu): Manages software packages.
    - `yum` / `dnf` (RHEL/CentOS): Manages software packages.
9. **Process Management**:
    
    - `ps`: Lists active processes.
    - `kill`: Terminates processes by PID.
    - `bg` / `fg`: Moves processes to the background or foreground.
    - `jobs`: Lists background jobs.
10. **Miscellaneous**:
    
    - `history`: Shows command history.
    - `alias`: Creates a shortcut for a command.

### Bash Operators:

1. **Arithmetic Operators**:
    
    - `+`: Addition.
    - `-`: Subtraction.
    - `*`: Multiplication.
    - `/`: Division.
    - `%`: Modulo.
    
    Example:
    
    bash
    
    Copy code
    
    `result=$((a + b))`
    
2. **Comparison Operators**:
    
    - `-eq`: Equal to.
    - `-ne`: Not equal to.
    - `-lt`: Less than.
    - `-le`: Less than or equal to.
    - `-gt`: Greater than.
    - `-ge`: Greater than or equal to.
    
    Example:
    
    bash
    
    Copy code
    
    `if [ $a -eq $b ]; then   echo "a is equal to b" fi`
    
3. **Logical Operators**:
    
    - `&&`: Logical AND.
    - `||`: Logical OR.
    - `!`: Logical NOT.
    
    Example:
    
    bash
    
    Copy code
    
    `if [ $a -gt 10 ] && [ $b -lt 5 ]; then   echo "Conditions met" fi`
    
4. **String Operators**:
    
    - `=`: Equal to.
    - `!=`: Not equal to.
    - `-z`: True if string is empty.
    - `-n`: True if string is not empty.
    
    Example:
    
    bash
    
    Copy code
    
    `if [ "$str1" = "$str2" ]; then   echo "Strings are equal" fi`
    
5. **Redirection Operators**:
    
    - `>`: Redirects output to a file (overwrite).
    - `>>`: Redirects output to a file (append).
    - `<`: Redirects input from a file.
    - `2>`: Redirects standard error to a file.
    
    Example:
    
    bash
    
    Copy code
    
    `command > output.txt  # Redirects output to file command >> output.txt # Appends output to file`
    
6. **Pipes** (`|`):
    
    - Pipes the output of one command as the input to another command.
    
    Example:
    
    bash
    
    Copy code
    
    `ls -l | grep "txt"`
    

### Suggested Workflow:

1. Start with **basic file commands** (`ls`, `cd`, `mkdir`).
2. Move on to **text processing commands** (`grep`, `awk`, `sed`).
3. Cover **basic operators** (comparison, logical, arithmetic).
4. Demonstrate **redirection** and **piping** with real examples.
5. Add a section on **scripts**, **conditionals**, and **loops**.


### 2. **Arithmetic Operators**:

Bash doesn't support floating-point arithmetic directly, but you can use `bc` or `awk` for such purposes. However, basic integer operations can be done using `((...))`.

- **Addition (`+`)**:
    
    bash
    
    Copy code
    
    `a=5 b=3 sum=$((a + b)) echo "Sum: $sum"  # Output: Sum: 8`
    
- **Subtraction (`-`)**:
    
    bash
    
    Copy code
    
    `a=10 b=4 diff=$((a - b)) echo "Difference: $diff"  # Output: Difference: 6`
    
- **Multiplication (`*`)**:
    
    bash
    
    Copy code
    
    `a=7 b=5 product=$((a * b)) echo "Product: $product"  # Output: Product: 35`
    
- **Division (`/`)**:
    
    bash
    
    Copy code
    
    `a=20 b=4 quotient=$((a / b)) echo "Quotient: $quotient"  # Output: Quotient: 5`
    
- **Modulo (`%`)**:
    
    bash
    
    Copy code
    
    `a=15 b=4 mod=$((a % b)) echo "Remainder: $mod"  # Output: Remainder: 3`
    

### 2. **Comparison Operators**:

These are primarily used in conditionals.

- **Equal to (`-eq`)**:
    
    bash
    
    Copy code
    
    `a=10 b=10 if [ $a -eq $b ]; then   echo "a is equal to b" fi`
    
- **Not equal to (`-ne`)**:
    
    bash
    
    Copy code
    
    `a=10 b=15 if [ $a -ne $b ]; then   echo "a is not equal to b" fi`
    
- **Less than (`-lt`)**:
    
    bash
    
    Copy code
    
    `a=5 b=10 if [ $a -lt $b ]; then   echo "a is less than b" fi`
    
- **Greater than (`-gt`)**:
    
    bash
    
    Copy code
    
    `a=15 b=10 if [ $a -gt $b ]; then   echo "a is greater than b" fi`
    
- **Less than or equal to (`-le`)**:
    
    bash
    
    Copy code
    
    `a=10 b=10 if [ $a -le $b ]; then   echo "a is less than or equal to b" fi`
    
- **Greater than or equal to (`-ge`)**:
    
    bash
    
    Copy code
    
    `a=20 b=15 if [ $a -ge $b ]; then   echo "a is greater than or equal to b" fi`
    

### 3. **String Operators**:

- **Equal (`=`)**:
    
    bash
    
    Copy code
    
    `str1="hello" str2="hello" if [ "$str1" = "$str2" ]; then   echo "Strings are equal" fi`
    
- **Not equal (`!=`)**:
    
    bash
    
    Copy code
    
    `str1="hello" str2="world" if [ "$str1" != "$str2" ]; then   echo "Strings are not equal" fi`
    
- **Check if string is empty (`-z`)**:
    
    bash
    
    Copy code
    
    `str="" if [ -z "$str" ]; then   echo "String is empty" fi`
    
- **Check if string is not empty (`-n`)**:
    
    bash
    
    Copy code
    
    `str="bash scripting" if [ -n "$str" ]; then   echo "String is not empty" fi`
    

### 4. **Logical Operators**:

- **AND (`&&`)**:
    
    bash
    
    Copy code
    
    `a=10 b=20 if [ $a -lt 15 ] && [ $b -gt 15 ]; then   echo "Both conditions are true" fi`
    
- **OR (`||`)**:
    
    bash
    
    Copy code
    
    `a=10 b=5 if [ $a -lt 5 ] || [ $b -gt 5 ]; then   echo "At least one condition is true" fi`
    
- **NOT (`!`)**:
    
    bash
    
    Copy code
    
    `a=10 if ! [ $a -eq 5 ]; then   echo "a is not equal to 5" fi`
    

### 5. **File Test Operators**:

- **Check if a file exists (`-e`)**:
    
    bash
    
    Copy code
    
    `file="data.txt" if [ -e "$file" ]; then   echo "File exists" fi`
    
- **Check if a file is readable (`-r`)**:
    
    bash
    
    Copy code
    
    `file="data.txt" if [ -r "$file" ]; then   echo "File is readable" fi`
    
- **Check if a file is writable (`-w`)**:
    
    bash
    
    Copy code
    
    `file="data.txt" if [ -w "$file" ]; then   echo "File is writable" fi`
    
- **Check if a file is executable (`-x`)**:
    
    bash
    
    Copy code
    
    `file="script.sh" if [ -x "$file" ]; then   echo "File is executable" fi`
    
- **Check if it's a directory (`-d`)**:
    
    bash
    
    Copy code
    
    `dir="/path/to/directory" if [ -d "$dir" ]; then   echo "It is a directory" fi`
    

### 6. **Redirection Operators**:

- **Redirect output to a file (`>`)**:
    
    bash
    
    Copy code
    
    `echo "This is a test" > output.txt  # Overwrites the file content`
    
- **Append output to a file (`>>`)**:
    
    bash
    
    Copy code
    
    `echo "Another line" >> output.txt  # Appends to the file`
    
- **Redirect input from a file (`<`)**:
    
    bash
    
    Copy code
    
    `while read line; do   echo "$line" done < input.txt`
    
- **Redirect standard error to a file (`2>`)**:
    
    bash
    
    Copy code
    
    `ls non_existing_file 2> error_log.txt  # Redirects error messages`
    
- **Redirect both stdout and stderr to a file**:
    
    bash
    
    Copy code
    
    `command > output.txt 2>&1`
    

### 7. **Piping (`|`)**:

- **Using pipes to pass output to another command**:
    
    bash
    
    Copy code
    
    `ps aux | grep "bash"`
    
- **Combining multiple commands**:
    
    bash
    
    Copy code
    
    `ls -l | grep "txt" | wc -l  # Counts the number of .txt files`
    

### 8. **Ternary Operator (Using `if` in One Line)**:

In Bash, there's no direct ternary operator like in other languages, but you can achieve similar functionality with a short `if` construct:

bash

Copy code

`[ $a -gt 10 ] && echo "a is greater than 10" || echo "a is less than or equal to 10"`

This gives you a solid foundation of Bash operators, which will be very useful in scripting workflows!