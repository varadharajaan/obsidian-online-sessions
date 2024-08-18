---
created: 2024-08-18T18:08
updated: 2024-08-18T18:15
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



Let’s dive into **loops**, **variables**, and some **intermediate operators** in Bash scripting. This will help in crafting more complex and useful scripts for your session.

### **1. Variables in Bash:**

- **Defining a Variable:**
    
    bash
    
    Copy code
    
    `name="Varad" age=30`
    
- **Using a Variable:**
    
    bash
    
    Copy code
    
    `echo "Hello, my name is $name and I am $age years old."`
    
- **Reading User Input:**
    
    bash
    
    Copy code
    
    `echo "Enter your name:" read name echo "Hello, $name!"`
    
- **Environment Variables:**
    
    bash
    
    Copy code
    
    `echo "Home directory: $HOME" echo "Current shell: $SHELL"`
    
- **Local Variables (Inside a Function)**:
    
    bash
    
    Copy code
    
    `my_function() {   local name="Local Name"   echo "Inside function: $name" } my_function echo "Outside function: $name"  # Won't show local name`
    

### **2. Loops in Bash:**

#### **For Loop**:

The `for` loop iterates over a list of items or a range of numbers.

- **Iterating over a list**:
    
    bash
    
    Copy code
    
    `for fruit in apple banana orange; do   echo "I like $fruit" done`
    
- **Iterating over a range of numbers**:
    
    bash
    
    Copy code
    
    `for i in {1..5}; do   echo "Number: $i" done`
    
- **Using C-style syntax**:
    
    bash
    
    Copy code
    
    `for ((i=1; i<=5; i++)); do   echo "Iteration: $i" done`
    
- **Looping over files in a directory**:
    
    bash
    
    Copy code
    
    `for file in *.txt; do   echo "Processing $file" done`
    

#### **While Loop**:

A `while` loop executes as long as a condition is true.

- **Basic while loop**:
    
    bash
    
    Copy code
    
    `count=1 while [ $count -le 5 ]; do   echo "Count: $count"   ((count++)) done`
    
- **Infinite while loop**:
    
    bash
    
    Copy code
    
    `while true; do   echo "Press [CTRL+C] to stop.."   sleep 1 done`
    

#### **Until Loop**:

The `until` loop runs until a condition becomes true.

- **Basic until loop**:
    
    bash
    
    Copy code
    
    `count=1 until [ $count -gt 5 ]; do   echo "Count: $count"   ((count++)) done`
    

### **3. Intermediate Operators in Bash:**

#### **Increment/Decrement (`++`, `--`)**:

- **Post-increment/Pre-increment**:
    
    bash
    
    Copy code
    
    `a=5 ((a++))  # Post-increment: use first, then increment echo $a  # Output: 6  ((++a))  # Pre-increment: increment first, then use echo $a  # Output: 7`
    
- **Post-decrement/Pre-decrement**:
    
    bash
    
    Copy code
    
    `b=5 ((b--))  # Post-decrement: use first, then decrement echo $b  # Output: 4  ((--b))  # Pre-decrement: decrement first, then use echo $b  # Output: 3`
    

#### **Conditional Statements within Loops**:

- **Using `if` inside a loop**:
    
    bash
    
    Copy code
    
    `for i in {1..10}; do   if [ $i -eq 5 ]; then     echo "Halfway there!"   else     echo "Number: $i"   fi done`
    

#### **Break and Continue**:

- **Break**: Exits the loop.
    
    bash
    
    Copy code
    
    `for i in {1..10}; do   if [ $i -eq 6 ]; then     echo "Breaking at $i"     break   fi   echo "Number: $i" done`
    
- **Continue**: Skips the rest of the loop and starts with the next iteration.
    
    bash
    
    Copy code
    
    `for i in {1..5}; do   if [ $i -eq 3 ]; then     echo "Skipping $i"     continue   fi   echo "Number: $i" done`
    

### **4. Arrays in Bash**:

Bash supports one-dimensional arrays.

- **Defining an array**:
    
    bash
    
    Copy code
    
    `fruits=("apple" "banana" "cherry")`
    
- **Accessing array elements**:
    
    bash
    
    Copy code
    
    `echo ${fruits[0]}  # Output: apple`
    
- **Looping through arrays**:
    
    bash
    
    Copy code
    
    `for fruit in "${fruits[@]}"; do   echo "I like $fruit" done`
    
- **Adding elements to an array**:
    
    bash
    
    Copy code
    
    `fruits+=("orange")`
    

### **5. Functions in Bash**:

Functions allow you to reuse code.

- **Defining a function**:
    
    bash
    
    Copy code
    
    `greet() {   echo "Hello, $1!" }`
    
- **Calling a function with arguments**:
    
    bash
    
    Copy code
    
    `greet "Varad"  # Output: Hello, Varad!`
    
- **Returning values** (return values as exit codes):
    
    bash
    
    Copy code
    
    `add() {   result=$(( $1 + $2 ))   return $result }  add 5 10 echo $?  # Output: 15 (exit status holds the value)`
    

### **6. Practical Bash Script Example**:

Let’s combine variables, loops, and conditionals into one practical script:

#### **Example: Simple Grading Script**

bash

Copy code

`#!/bin/bash  # Function to determine grade based on score get_grade() {     score=$1     if [ $score -ge 90 ]; then         echo "A"     elif [ $score -ge 80 ]; then         echo "B"     elif [ $score -ge 70 ]; then         echo "C"     elif [ $score -ge 60 ]; then         echo "D"     else         echo "F"     fi }  # Loop to input student scores while true; do     echo -n "Enter student score (or type 'exit' to quit): "     read score      if [[ "$score" == "exit" ]]; then         echo "Exiting the script!"         break     elif ! [[ "$score" =~ ^[0-9]+$ ]]; then         echo "Invalid input! Please enter a valid number."     else         grade=$(get_grade $score)         echo "The grade is: $grade"     fi done`

### **7. Handling Command-Line Arguments**:

Bash scripts can take input parameters from the command line.

- **Using command-line arguments**:
    
    bash
    
    Copy code
    
    `echo "Script name: $0" echo "First argument: $1" echo "Second argument: $2"`
    
- **Using `$@` to loop over all arguments**:
    
    bash
    
    Copy code
    
    `for arg in "$@"; do   echo "Argument: $arg" done`


Here are some **Bash file operations** to perform **CRUD tasks** and work with **numbers in a file**:

### **1. Reading a File**:

You can use the `cat`, `while` loop, or `read` command to read a file line by line.

- **Example: Read and print each line from a text file**:
    
    bash
    
    Copy code
    
    `# reading a file using a while loop filename="numbers.txt" while read -r line; do   echo "Line: $line" done < "$filename"`
    
- **Using `cat`**:
    
    bash
    
    Copy code
    
    `cat numbers.txt`
    

### **2. Creating or Writing to a File**:

- **Create a new file and write content to it**:
    
    bash
    
    Copy code
    
    `echo "Hello World!" > newfile.txt`
    
- **Append content to a file**:
    
    bash
    
    Copy code
    
    `echo "This is appended text." >> newfile.txt`
    

### **3. Updating a File**:

Updating specific lines or content in a file requires tools like `sed`.

- **Replace text in a file (inline update)**:
    
    bash
    
    Copy code
    
    `sed -i 's/old_text/new_text/g' file.txt`
    
- **Replace a specific line (line number)**:
    
    bash
    
    Copy code
    
    `sed -i '3s/.*/Updated content/' file.txt  # Updates line 3`
    

### **4. Deleting Lines from a File**:

- **Delete specific lines using `sed`**:
    
    bash
    
    Copy code
    
    `sed -i '3d' file.txt  # Deletes the 3rd line`
    
- **Delete lines matching a pattern**:
    
    bash
    
    Copy code
    
    `sed -i '/pattern/d' file.txt`
    

### **5. Reading a File with a List of Numbers and Summing Them**:

- **Example: Reading numbers from a file and calculating the sum**: Suppose `numbers.txt` contains a list of numbers:
    
    Copy code
    
    `10 20 30 40`
    
    You can sum them up using a loop:
    
    bash
    
    Copy code
    
    `sum=0 while read -r number; do   sum=$((sum + number)) done < numbers.txt echo "Total sum: $sum"`
    

### **6. Creating and Iterating Over Files**:

- **Create a file with a list of numbers**:
    
    bash
    
    Copy code
    
    `echo -e "10\n20\n30\n40" > numbers.txt`
    
- **Read the file and calculate the sum**:
    
    bash
    
    Copy code
    
    `sum=0 while IFS= read -r number; do   sum=$((sum + number)) done < numbers.txt echo "Sum of numbers: $sum"`
    

### **7. CRUD Operations with Text Files**:

- **Create a file**:
    
    bash
    
    Copy code
    
    `echo "Employee Name,Location,Salary,Position" > employees.csv echo "Varad,Pune,70000,Engineer" >> employees.csv echo "Alex,Delhi,60000,Analyst" >> employees.csv`
    
- **Read from the file**:
    
    bash
    
    Copy code
    
    `while IFS=, read -r name location salary position; do   echo "Name: $name, Location: $location, Salary: $salary, Position: $position" done < employees.csv`
    
- **Update the file (e.g., replace salary)**:
    
    bash
    
    Copy code
    
    `sed -i 's/60000/65000/' employees.csv`
    
- **Delete a line from the file**:
    
    bash
    
    Copy code
    
    `sed -i '/Alex/d' employees.csv`
    

### **8. File Existence and Permissions**:

- **Check if a file exists**:
    
    bash
    
    Copy code
    
    `if [ -f "file.txt" ]; then   echo "File exists." else   echo "File does not exist." fi`
    
- **Check if a directory exists**:
    
    bash
    
    Copy code
    
    `if [ -d "/path/to/dir" ]; then   echo "Directory exists." fi`
    

### **9. Reading and Modifying File Permissions**:

- **Changing file permissions**:
    
    bash
    
    Copy code
    
    `chmod 644 myfile.txt  # Read and write for owner, read-only for others`
    
- **Checking file permissions**:
    
    bash
    
    Copy code
    
    `ls -l myfile.txt`
    

### **10. Example: Simple CRUD Bash Script for Employees**

This script allows adding, reading, and removing employees from a CSV file.

bash

Copy code

`#!/bin/bash  file="employees.csv"  # Initialize file with headers if it doesn't exist if [ ! -f "$file" ]; then     echo "Name,Location,Salary,Position" > "$file" fi  # Functions for CRUD operations add_employee() {     echo "Enter name:"     read name     echo "Enter location:"     read location     echo "Enter salary:"     read salary     echo "Enter position:"     read position     echo "$name,$location,$salary,$position" >> "$file"     echo "Employee added." }  list_employees() {     echo "List of employees:"     cat "$file" }  delete_employee() {     echo "Enter the name of the employee to delete:"     read name     sed -i "/$name/d" "$file"     echo "Employee $name deleted." }  # Menu for user interaction while true; do     echo "1. Add Employee"     echo "2. List Employees"     echo "3. Delete Employee"     echo "4. Exit"     read choice      case $choice in         1) add_employee ;;         2) list_employees ;;         3) delete_employee ;;         4) break ;;         *) echo "Invalid option." ;;     esac done`

### Summary:

- **Basic file operations**: Read, create, write, append, and delete.
- **Text processing with `sed`**: To update and remove specific lines or patterns.
- **Summing numbers**: Using loops to process numeric data from a file.
- **Simple CRUD operations**: With CSV files for employee management.

These examples will provide your learners with hands-on experience in manipulating files and using Bash scripting effectively for various tasks.


**Bash script** that reads two lines from a file where each line contains comma-separated numbers, calculates the sum for each line, and prints the result.

### Example File (`numbers.txt`):

Copy code

`10,20,30,40 5,15,25,35`

### Bash Script to Add and Print Sum:

bash

Copy code

`#!/bin/bash  # File containing comma-separated numbers file="numbers.txt"  # Read the first and second lines from the file line1=$(sed -n '1p' $file) line2=$(sed -n '2p' $file)  # Function to calculate the sum of a comma-separated line calculate_sum() {     local sum=0     IFS=',' read -ra numbers <<< "$1"     for number in "${numbers[@]}"; do         sum=$((sum + number))     done     echo $sum }  # Calculate and print the sum for line 1 sum_line1=$(calculate_sum "$line1") echo "Line 1 sum is: $sum_line1"  # Calculate and print the sum for line 2 sum_line2=$(calculate_sum "$line2") echo "Line 2 sum is: $sum_line2"`

### Explanation:

- **`sed -n '1p'`**: Fetches the first line from the file.
- **`sed -n '2p'`**: Fetches the second line from the file.
- **`IFS=',' read -ra numbers <<< "$1"`**: Splits the line by commas into an array.
- **`sum=$((sum + number))`**: Adds each number in the array.

### Output for the file `numbers.txt`:

python

Copy code

`Line 1 sum is: 100 Line 2 sum is: 80`

This script processes the two lines, sums the numbers, and prints the result for both lines.



**Bash script** to search for a specific word in a file, count its occurrences, and print the result. The script will print the count if the word is found or state "Not present" if the word is not found.

### Example Text File (`words.txt`):

Copy code

`apple orange banana apple mango grape apple banana apple orange grape mango mango orange apple`

### Bash Script:

bash

Copy code

`#!/bin/bash  # File containing words file="words.txt"  # Ask the user for the word to search echo "Enter the word to search:" read word  # Search for the word and count its occurrences count=$(grep -o -w "$word" "$file" | wc -l)  # Check if the word was found and print the appropriate message if [ "$count" -gt 0 ]; then     echo "The word '$word' occurs $count times." else     echo "The word '$word' is not present." fi`

### Explanation:

- **`grep -o -w "$word" "$file"`**: Searches for the exact word in the file (`-w` ensures whole-word match, and `-o` outputs only the matching words).
- **`wc -l`**: Counts the number of lines, effectively counting how many times the word appears.
- **`if [ "$count" -gt 0 ]`**: Checks if the word is found (`count` is greater than zero).

### Example:

#### Input:

arduino

Copy code

`Enter the word to search: apple`

#### Output:

arduino

Copy code

`The word 'apple' occurs 4 times.`

#### Input:

arduino

Copy code

`Enter the word to search: pear`

#### Output:

arduino

Copy code

`The word 'pear' is not present.`

This script efficiently searches for the word and provides the count or notifies if it's not found.