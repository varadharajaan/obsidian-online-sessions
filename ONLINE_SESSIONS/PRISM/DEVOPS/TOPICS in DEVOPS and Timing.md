---
created: 2024-08-15T17:34
updated: 2024-11-11T22:24
---
## Types of Linux File System

There is a wide range of file systems available in Linux, each of which is designed to meet specific needs. We will learn about some of the most common file systems in Linux below :

IOPS - input output processing per second

- **ext2:**  
    The ext2 (extended file system 2) is one of the oldest and most widely used Linux file systems. It has been the default file system for most Linux distributions for many years. The ext2 file system does not have a journal, which means that file recovery can be more difficult after a system crash. However, it is a stable and reliable file system that is ideal for small to medium-sized partitions.
- **ext3:**  
    The ext3 (extended file system 3) is an extension of the ext2 file system that adds journaling support. Journaling keeps track of changes to the file system, which helps to reduce the risk of data loss after a system crash. The ext3 file system is widely used and is a good choice for most Linux installations. It is stable, reliable, and has good performance.
- **ext4:**  
    The ext4 (extended file system 4) is the successor to the ext3 file system and was designed to address some of the limitations of ext3. It supports larger file sizes, faster file system checks, and better performance on large disks. It also includes journal checksumming, which improves data integrity. The ext4 file system is the default file system used by many modern Linux distributions.
- **XFS:**  
    The XFS(X File System) is a high-performance file system designed for large-scale storage systems. It supports file systems up to 16 exabytes in size, making it suitable for use in large data centers. The XFS file system is known for its scalability, performance, and reliability. It supports advanced features such as journaling, file-level encryption, and online defragmentation.
- **Btrfs:**  
    The Btrfs (B-tree file system) is a modern file system designed for use on Linux systems. It supports features such as copy-on-write, snapshots, and subvolumes, which allow users to create separate file systems within a single partition. It also includes built-in support for RAID and compression. Btrfs is still under active development and is not yet as widely used as some of the other file systems.
- **ZFS:**  
    The ZFS (Zettabyte File System) is a powerful and feature-rich file system that was originally developed for Solaris. It supports advanced features such as snapshots, data compression, deduplication, and built-in RAID. ZFS is known for its reliability and data integrity features, including checksumming and self-healing capabilities. It is not included in most Linux distributions by default due to licensing issues but can be installed separately.
- **JFS:**  
    The JFS(Journaled File System) is a high-performance file system that was originally developed by IBM. It includes advanced features such as journaling, file-level compression, and online resizing. The JFS file system is known for its speed and reliability and is a good choice for high-performance computing systems.
- **ReiserFS:**  
    The ReiserFS is a file system that was designed for high-performance computing systems. It includes advanced features such as journaling, file-level encryption, and support for large files and directories. The ReiserFS file system is known for its speed and reliability but is not as widely used as some of the other file systems on this list


1. Root Directory (/): As mentioned earlier, the root directory is the starting point of the entire Linux filesystem. All other directories, files, and devices are organized under this directory.

2. /bin: This directory contains essential binary executable files, such as basic commands like 'ls', 'cp', 'mv', and 'rm', which are required for system operation and maintenance.

3. /boot: The /boot directory holds files related to the boot process, including the Linux kernel and bootloader configuration files.

4. /dev: Short for "devices," the /dev directory contains special files that represent hardware devices such as hard drives, terminals, and printers. These files facilitate communication between the operating system and the hardware devices.

5. /etc: The /etc directory stores system-wide configuration files and scripts used by the system administrator for system maintenance and customization.

6. /home: Each user on a Linux system has a personal directory within the /home directory. This is where users store their personal files, settings, and configurations.

7. /lib: The /lib directory contains shared library files required by various programs and the kernel to function correctly.

8. /media: In the /media directory, removable media devices like USB drives, CDs, and DVDs are automatically mounted when inserted into the system.

9. /opt: The /opt directory is designated for optional software packages and third-party applications that are not part of the default Linux installation.

10. /proc: The /proc directory is a virtual filesystem that provides information about running processes and system resources.

11. /sbin: Similar to the /bin directory, the /sbin directory contains essential system binary files. However, these files are specifically for system administration tasks and are typically used by the root user.

12. /tmp: The /tmp directory is a temporary storage location for files created by various programs during their operation. These files are automatically deleted upon system reboot.

13. /usr: The /usr directory contains non-essential files such as user-installed applications, libraries, and documentation.

14. /var: The /var directory stores variable data files, such as log files, email queues, and databases, that change frequently during system operation.

----------------------------------------------------------------------

Here’s a detailed explanation of each folder in the Linux file system:

1. / (Root Directory)
The root directory is the starting point of the Linux file system. All other directories and files stem from this directory.

Example Files: None, it's just the root.
Usage: Contains essential directories like /bin, /etc, and /usr.
2. /bin (Binaries)
Contains essential user command binaries (executables) required during boot and in single-user mode.

Example Files: ls (list directory contents), cp (copy files), mv (move files), cat (concatenate files), bash (Bash shell).
Usage: Commands required for the system to function, even in minimal environments.
3. /boot (Boot Files)
Holds files needed for the system to boot, including the Linux kernel and bootloader configuration files.

Example Files: vmlinuz (compressed Linux kernel), initrd.img (initial RAM disk image), grub.conf (GRUB bootloader configuration).
Usage: Essential files for the boot process. Without these, the system can’t start.
4. /dev (Device Files)
Contains special device files representing hardware components and pseudo-devices like terminals or drives.

Example Files: sda (first hard disk), tty (terminals), null (null device), random (random number generator).
Usage: Provides an interface to devices. The kernel manages these files dynamically.
5. /etc (Configuration Files)
This directory contains all configuration files and shell scripts required to boot and configure system settings.

Example Files: passwd (user account information), fstab (file system mounting information), hosts (hostname and IP mappings), resolv.conf (DNS configuration).
Usage: Core configuration files that control system behavior and settings.
6. /home (Home Directories)
Holds the home directories of individual users. Each user has a personal directory where their files are stored.

Example Files: User-specific files like ~/Documents/, ~/Pictures/, ~/Downloads/, ~/.bashrc (user-specific bash configuration).
Usage: Personal storage space for each user. Users can store personal documents, configurations, and files.
7. /lib (Libraries)
Contains shared libraries needed by the binaries in /bin and /sbin. These are essential for the basic system functionality.

Example Files: libc.so.6 (standard C library), ld-linux.so.2 (dynamic linker).
Usage: Stores system libraries that help programs execute.
8. /media (Removable Media)
Used as a mount point for external drives, such as USB sticks, CD-ROMs, and other removable media.

Example Files: /media/usb-drive/ (mounted USB stick), /media/cdrom/ (mounted CD).
Usage: External media automatically mount here when connected.
9. /mnt (Mount Directory)
Another directory where temporary file systems can be mounted. Typically used by system administrators for manual mounts.

Example Files: Custom mount points like /mnt/mydisk/.
Usage: Commonly used to manually mount file systems during maintenance.
10. /opt (Optional Software)
Stores optional third-party software and add-on applications that are not part of the default installation.

Example Files: Software packages like /opt/google/ for Google Chrome, /opt/vmware/ for VMware tools.
Usage: For installing extra software that’s not managed by the system’s package manager.
11. /proc (Process Information)
A virtual file system that contains runtime system information (e.g., system memory, hardware configuration, and running processes).

Example Files: cpuinfo (CPU information), meminfo (memory usage), pid/ (process information for process ID).
Usage: Provides information and configuration details about the running kernel and system processes.
12. /root (Root User’s Home)
This is the home directory of the root user (the superuser).

Example Files: /root/.bashrc (root's bash configuration), /root/.ssh/ (SSH configuration).
Usage: Used as the administrative user’s home directory for private files and configurations.
13. /run (Runtime Information)
Stores volatile runtime data used by processes and applications since the last boot. This is a temporary filesystem that gets cleared on reboot.

Example Files: utmp (list of logged-in users), systemd/ (system and service manager data).
Usage: Holds runtime information about the system and services like PIDs or lock files.
14. /sbin (System Binaries)
Contains essential binaries for system administration, such as system utilities required by the root user.

Example Files: fsck (file system check), ifconfig (network configuration), reboot (reboots the system).
Usage: Commands used by the system administrator to manage and maintain the system.
15. /srv (Service Data)
Holds data for services provided by the system, like web servers and FTP servers.

Example Files: /srv/www/ (web server files), /srv/ftp/ (FTP files).
Usage: Used to store data served by the system to external users.
16. /sys (System Information)
Another virtual file system that provides information about the system’s hardware and kernel.

Example Files: /sys/block/ (block devices), /sys/class/ (kernel classes).
Usage: Contains data about devices, kernel modules, and more.
17. /tmp (Temporary Files)
Stores temporary files that are created by users or programs. This directory is typically cleared on system reboot.

Example Files: /tmp/tmpfile.txt (temporary file), /tmp/some_program_socket (temporary socket file).
Usage: Used by applications to store temporary files during processing.
18. /usr (User Programs)
Contains user binaries, documentation, libraries, and source code. It’s divided into subdirectories like /usr/bin/, /usr/lib/, /usr/share/, and /usr/local/.

Example Files: /usr/bin/gcc (C compiler), /usr/share/man (man pages), /usr/lib (libraries).
Usage: Stores system-wide application data, binaries, and libraries for user applications.
19. /var (Variable Files)
Contains files that are expected to grow in size over time, such as logs, mail spools, and cached data.

Example Files: log/ (system logs like /var/log/syslog), spool/ (print spools), cache/ (cached data).
Usage: Stores log files, cached files, and other variable files that change frequently during system operation.
Each directory in this structure is designed to hold specific types of files and directories, making Linux both organized and modular.>)

![[Pasted image 20240817173316.png]]

object storage
file system
block storage

SFTP 
FTP servers

mnt commands
dsf -h 
lstbk



