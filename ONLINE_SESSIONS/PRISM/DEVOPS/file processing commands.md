---
created: 2024-08-17T17:52
updated: 2024-08-17T18:01
---

[](<# File Searching and Processing Commands Cheat Sheet

## Sample File
Use the provided `chec.txt` file for running the following commands.

## Basic File Processing Commands

### 1. `cat` - Display File Content
- Command: `cat chec.txt`
  - This command will display the entire content of the file.

### 2. `grep` - Search for Patterns
- Command: `grep "sample" chec.txt`
  - This command will search for the word "sample" in the file.

### 3. `awk` - Text Processing and Pattern Scanning
- Command: `awk '{print $1}' chec.txt`
  - This command will print the first word of each line from `chec.txt`.
- Command: `awk '/sample/ {print $0}' chec.txt`
  - This command will print all lines containing the word "sample".

### 4. `sed` - Stream Editing
- Command: `sed 's/sample/TEST/g' chec.txt`
  - This command will replace all occurrences of the word "sample" with "TEST" in the file.
- Command: `sed -n '3,5p' chec.txt`
  - This command will print lines 3 to 5 from the file.

### 5. `find` - Search for Files
- Command: `find . -name "chec.txt"`
  - This command will search for the file named `chec.txt` in the current directory.

### 6. `cut` - Cut Specific Columns from a File
- Command: `cut -d' ' -f1 chec.txt`
  - This command will extract the first word from each line, using a space as the delimiter.

### 7. `sort` - Sort File Contents
- Command: `sort chec.txt`
  - This command will sort the lines in the file alphabetically.

### 8. `uniq` - Remove Duplicate Lines
- Command: `uniq chec.txt`
  - This command will remove consecutive duplicate lines from the file.

### 9. `wc` - Word Count
- Command: `wc -l chec.txt`
  - This command will count the number of lines in the file.
- Command: `wc -w chec.txt`
  - This command will count the number of words in the file.

## Advanced Examples

### 10. `awk` - Conditional Processing
- Command: `awk '$1 == "The" {print $0}' chec.txt`
  - This command will print all lines where the first word is "The".

### 11. `sed` - Append/Insert Text
- Command: `sed '1i\This is an inserted line' chec.txt`
  - This command will insert the text at the top of the file.>)



**playground commands:**
grep -o "dog" chec.txt | wc -l
awk '/dog/' filename
sed -n '/dog/p' filename
grep 'dog' filename
grep -i 'dog' filename
grep -r 'dog' directory_name
sed -n '/dog/p' filename | wc -l
awk '/dog/' filename | wc -l

