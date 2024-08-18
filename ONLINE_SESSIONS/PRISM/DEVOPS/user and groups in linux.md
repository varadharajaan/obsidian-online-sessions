---
created: 2024-08-18T18:21
updated: 2024-08-18T18:22
---


### 1. **Create a New User and Group**

bash

Copy code

`# Create a new user sudo adduser varad # Create a new group sudo groupadd devgroup # Add the user to the new group sudo usermod -aG devgroup varad`

You can log in as the new user with:

bash

Copy code

`su - varad`

### 2. **Change File Ownership to a User**

bash

Copy code

`# Create a file touch file1.txt # Change the ownership of the file to user 'varad' sudo chown varad file1.txt # Check the ownership ls -l file1.txt`

### 3. **Change File Ownership to a Group**

bash

Copy code

`# Change the group ownership of the file to 'devgroup' sudo chown :devgroup file1.txt # Check the ownership ls -l file1.txt`

### 4. **Change Ownership for Both User and Group**

bash

Copy code

`# Change both user and group ownership of a file sudo chown varad:devgroup file1.txt # Check the ownership ls -l file1.txt`

### 5. **Give Read, Write, and Execute Permissions to the User**

bash

Copy code

`# Give read, write, and execute permissions to the file owner chmod u+rwx file1.txt # Check the file permissions ls -l file1.txt`

### 6. **Remove Write Permission for Group and Others**

bash

Copy code

`# Remove write permission for group and others chmod go-w file1.txt # Check the file permissions ls -l file1.txt`

### 7. **Grant Full Permissions to Everyone**

bash

Copy code

`# Give read, write, and execute permissions to everyone (user, group, others) chmod 777 file1.txt # Check the file permissions ls -l file1.txt`

### 8. **Set Permissions Using Octal Notation**

bash

Copy code

`# Give read and write to user, read to group, no permissions to others (chmod 640) chmod 640 file1.txt # Check the file permissions ls -l file1.txt`

### 9. **Recursive Chown for Directories and Files**

bash

Copy code

`# Create a directory mkdir mydir # Change ownership of directory and all its contents recursively sudo chown -R varad:devgroup mydir/ # Check the ownership of directory ls -ld mydir/`

### 10. **Restrict File Access to Owner Only**

bash

Copy code

`# Remove all permissions for group and others chmod go-rwx file1.txt # Check the file permissions ls -l file1.txt`

### Bonus Commands:

- To switch to the newly created user `varad`:

bash

Copy code

`su - varad`

- To list the groups of a user:

bash

Copy code

`groups varad`

These commands will give you practical experience in managing users, groups, and permissions in a Linux environment!


To check if the new user `deepak` can edit a file created by `varad`, follow these steps:

### 1. **Create a New User: `deepak`**

bash

Copy code

`sudo adduser deepak`

Set the password when prompted. You can now log in as `deepak` using:

bash

Copy code

`su - deepak`

### 2. **Create a File as `varad`**

Log back in as `varad` and create a file:

bash

Copy code

`su - varad touch file2.txt echo "This is a file created by varad." > file2.txt`

### 3. **Set Permissions for the File**

Check the file permissions:

bash

Copy code

`ls -l file2.txt`

By default, only the owner (`varad`) can edit the file. The `deepak` user will not be able to modify it unless permissions are changed.

### 4. **Log in as `deepak` and Try to Edit the File**

Switch to the `deepak` user:

bash

Copy code

`su - deepak`

Attempt to edit the file:

bash

Copy code

``nano file2.txt  # or use `vim` or any other editor``

You should get a "Permission denied" message because `deepak` doesn’t have write permission.

### 5. **Grant `deepak` Write Permissions**

Switch back to `varad`:

bash

Copy code

`su - varad`

You can either:

- Change the group ownership to a group that includes both `varad` and `deepak`:

bash

Copy code

`sudo chown :devgroup file2.txt sudo chmod g+w file2.txt`

- Or give `others` (which includes `deepak`) write permissions:

bash

Copy code

`sudo chmod o+w file2.txt`

### 6. **Test the Changes as `deepak`**

Now log back in as `deepak` and try editing the file again:

bash

Copy code

`su - deepak nano file2.txt`

### 7. **Restrict Permissions Again (Optional)**

Once `deepak` has edited the file, you can restrict the permissions back to prevent further changes:

bash

Copy code

`su - varad chmod o-w file2.txt`

This workflow will allow you to check and understand how file ownership and permissions work between different users.