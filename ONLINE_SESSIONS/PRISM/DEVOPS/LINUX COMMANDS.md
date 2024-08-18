---
created: 2024-08-17T17:44
updated: 2024-08-18T00:22
---
[](<# Basic Linux Commands Cheat Sheet

## Basic Commands
1. **ls** – List directory contents.
   - Example: `ls -l` (long listing format)
2. **cd** – Change directory.
   - Example: `cd /var/log`
3. **pwd** – Print current working directory.
   - Example: `pwd`
4. **touch** – Create an empty file.
   - Example: `touch newfile.txt`
5. **cp** – Copy files or directories.
   - Example: `cp file1.txt file2.txt`
6. **mv** – Move or rename files or directories.
   - Example: `mv file.txt /home/user/`
7. **rm** – Remove files or directories.
   - Example: `rm -r folder/` (recursive deletion)
8. **cat** – Concatenate and display file content.
   - Example: `cat file.txt`
9. **more** – View file content one screen at a time.
   - Example: `more file.txt`
10. **less** – View file content with navigation.
    - Example: `less file.txt`

## File and Directory Permissions
11. **chmod** – Change file permissions.
    - Example: `chmod 755 script.sh`
12. **chown** – Change file owner and group.
    - Example: `chown user:group file.txt`
13. **umask** – Set default file creation permissions.
    - Example: `umask 022`



## File Searching and Processing
14. **find** – Search for files.
    - Example: `find /home -name "*.log"`
15. **grep** – Search within files.
    - Example: `grep "search_term" file.txt`
16. **awk** – Text processing and pattern scanning.
    - Example: `awk '{print $1}' file.txt`
17. **sed** – Stream editor for editing text.
    - Example: `sed 's/old/new/g' file.txt`

## Disk and System Information
18. **df** – Show disk usage.
    - Example: `df -h` (human-readable format)
19. **du** – Estimate file space usage.
    - Example: `du -sh folder/`
20. **top** – Display system tasks in real-time.
    - Example: `top`
21. **htop** – Interactive process viewer.
    - Example: `htop`
22. **free** – Show memory usage.
    - Example: `free -m`
23. **uname** – Show system information.
    - Example: `uname -a`

## Process Management
24. **ps** – Display running processes.
    - Example: `ps aux`
25. **kill** – Terminate a process by PID.
    - Example: `kill 1234`
26. **killall** – Terminate all processes by name.
    - Example: `killall firefox`
27. **bg** – Resume a suspended job in the background.
    - Example: `bg %1`
28. **fg** – Bring a background job to the foreground.
    - Example: `fg %1`

## Networking
29. **ping** – Check network connectivity.
    - Example: `ping google.com`
30. **ifconfig** – Configure network interfaces.
    - Example: `ifconfig eth0`
31. **curl** – Transfer data from URLs.
    - Example: `curl -O http://example.com/file.zip`
32. **scp** – Securely copy files between hosts.
    - Example: `scp file.txt user@remote:/path`
33. **ssh** – Securely connect to a remote server.
    - Example: `ssh user@server`

## Compression and Archiving
34. **tar** – Archive files.
    - Example: `tar -czvf archive.tar.gz folder/`
    - to view the files [in the archive: `tar -tvf archive.tar.gz`]
1. **gzip** – Compress files using gzip.
    - Example: `gzip file.txt`
2. **unzip** – Extract a zip archive.
    - Example: `unzip archive.zip`

## Package Management
37. **apt-get** – Install or remove packages (Debian/Ubuntu).
    - Example: `sudo apt-get install package_name`
38. **yum** – Install or remove packages (RedHat/CentOS).
    - Example: `sudo yum install package_name`
39. **dpkg** – Install .deb packages.
    - Example: `sudo dpkg -i package.deb`
40. **rpm** – Install .rpm packages.
    - Example: `sudo rpm -i package.rpm`

## User Management
41. **adduser** – Add a new user.
    - Example: `sudo adduser newuser`
42. **passwd** – Change user password.
    - Example: `passwd username`
43. **userdel** – Delete a user.
    - Example: `sudo userdel username`

## Shutdown and Reboot
44. **shutdown** – Shutdown the system.
    - Example: `sudo shutdown -h now`
45. **reboot** – Reboot the system.
    - Example: `sudo reboot`

## Ownership Examples:
1. **chown john:developers report.txt**
   - Change the owner to `john` and the group to `developers` for the file `report.txt`.

2. **chown john report.txt**
   - Change only the user ownership to `john` for the file `report.txt`.

3. **chown :developers report.txt**
   - Change only the group ownership to `developers` for the file `report.txt`.

4. **chown -R john:developers /var/www/html**
   - Recursively change the ownership of all files and subdirectories inside `/var/www/html` to `john:developers`.

5. **chgrp developers report.txt**
   - Change only the group ownership to `developers` for the file `report.txt`.>)
sudo groupadd developers
sudo useradd -g groupname username
sudo passwd username

sudo useradd -g developers john

check group
grep 'groupname' /etc/group

check user
grep 'username' /etc/passwd

change user permissions to a file
sudo chown john:developers report.txt



