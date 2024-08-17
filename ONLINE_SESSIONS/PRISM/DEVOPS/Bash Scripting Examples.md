---
created: 2024-08-17T18:06
updated: 2024-08-17T18:10
---
**Simple Calculator:** Write a bash script that takes two numbers and an operator (`+`, `-`, `*`, `/`) as input and performs the corresponding arithmetic operation.
```
#!/bin/bash
read -p "Enter first number: " num1
read -p "Enter second number: " num2
read -p "Enter operator (+, -, *, /): " op

case $op in
  +) result=$(echo "$num1 + $num2" | bc);;
  -) result=$(echo "$num1 - $num2" | bc);;
  \*) result=$(echo "$num1 * $num2" | bc);;
  /) result=$(echo "scale=2; $num1 / $num2" | bc);;
  *) echo "Invalid operator"; exit 1;;
esac

echo "Result: $result"
```

**List Files and Directories:** Write a bash script that lists all files and directories in the current directory and counts them.

```
#!/bin/bash
echo "Files and directories in the current directory:"
ls
echo "Total count: $(ls | wc -l)"

```

**File Existence Check:** Write a bash script that checks if a file exists. If it does, print "File exists"; otherwise, print "File does not exist."

```
#!/bin/bash
read -p "Enter the filename: " filename
if [ -e "$filename" ]; then
  echo "File exists"
else
  echo "File does not exist"
fi

```

**Hello World Script:** Write a bash script that prints "Hello, World!" to the termina

```
#!/bin/bash
echo "Hello, World!"

```


**process monitoring**
Write a bash script that checks if a specified process is running. If it is, print "Process is running"; otherwise, print "Process is not running."

```
#!/bin/bash
read -p "Enter the process name: " process_name
if pgrep "$process_name" > /dev/null; then
  echo "Process is running"
else
  echo "Process is not running"
fi

```
**User Directory Cleanup:** Write a bash script that deletes files in a user's home directory that are older than 30 days.
```
#!/bin/bash
find ~/ -type f -mtime +30 -exec rm {} \;
echo "Old files deleted from your home directory."

```
**Log File Analysis:** Write a bash script that takes a log file as input and counts the number of occurrences of the word "ERROR."

```
#!/bin/bash
read -p "Enter the log file name: " log_file
if [ -f "$log_file" ]; then
  error_count=$(grep -o "ERROR" "$log_file" | wc -l)
  echo "Number of occurrences of 'ERROR': $error_count"
else
  echo "File does not exist"
fi

```
**Backup Script:** Write a bash script that backs up a directory to a specified backup location. The script should create a timestamped tarball of the directory.

```
#!/bin/bash
read -p "Enter the directory to backup: " dir
read -p "Enter the backup location: " backup_dir

timestamp=$(date +"%Y%m%d%H%M%S")
tar -czf "$backup_dir/backup_$timestamp.tar.gz" "$dir"

echo "Backup completed: $backup_dir/backup_$timestamp.tar.gz">)
```
