Basic Commands Used in Linux: 
--

- whoami command - This command tells you about who is the user

<img width="440" height="63" alt="image" src="https://github.com/user-attachments/assets/6226e66b-fe6f-46d7-8943-db1befa1a994" />



- pwd - present working directory

<img width="396" height="129" alt="image" src="https://github.com/user-attachments/assets/8df36f34-3e86-46be-a07b-0bca6590443a" />


- ls - Listing the files

<img width="553" height="85" alt="image" src="https://github.com/user-attachments/assets/2f0e57dc-a4d0-4544-892d-d677aa44c9db" />


- cat Command - It is used to print the content of the file

<img width="954" height="274" alt="image" src="https://github.com/user-attachments/assets/d7dbe5a7-d117-4795-9603-2ad9666596a5" />


How to switch into Root User ? 
--

- sudo -i - This command is used to switch into an root user


<img width="422" height="134" alt="image" src="https://github.com/user-attachments/assets/8d3703c2-272b-4e74-9fea-75bad30a0c5b" />



LINUX FILE SYSTEM :
-------
- The Linux File System is the way Linux organizes, stores, and manages files and directories.

- In Linux:

   - Everything is treated as a file - Regular files, Directories, Devices, Processes

   - Files are organized in a hierarchical structure

   - It starts from a single root directory → /

- Unlike Windows (C:, D: drives), Linux has one single tree structure.


 <img width="728" height="590" alt="image" src="https://github.com/user-attachments/assets/c7d6f7db-5a2c-4ad7-9f27-0df1f54be271" />


- cd command - This command is said to be an changing directory

<img width="1233" height="96" alt="image" src="https://github.com/user-attachments/assets/01a75a6d-37ca-494a-9075-209ed8cc7d61" />

The above mentioned Images shows you the File system of the linux 


| Directory | Purpose | Real-Time DevOps Usage |
|-----------|----------|------------------------|
| / | Root directory (top level). Base of entire file system. | Starting point of Linux structure |
| /bin | Essential user command binaries (ls, cp, mv). | Used for basic command execution |
| /sbin | System binaries (root user commands). | System-level administration (reboot, fdisk, iptables) |
| /boot | Boot loader files & Linux kernel. | Kernel updates & boot troubleshooting |
| /dev | Device files (hard disk, USB, etc.). | Disk and hardware management |
| /etc | Configuration files. | Service & application configuration management |
| /home | User home directories. | Stores user data and project files |
| /root | Root user's home directory. | Admin-level operations |
| /lib | System libraries required by binaries. | Dependency management for applications |
| /usr | User programs & utilities. | Installed software binaries |
| /opt | Optional / third-party software packages. | Custom software installations |
| /var | Log files & variable data (logs, spool, cache). | Log monitoring & troubleshooting (/var/log) |
| /tmp | Temporary files. | Temporary script execution & testing |
| /proc | Virtual file system containing process info. | System & process monitoring |
| /mnt | Temporary mount point for file systems. | Manually mounting storage devices |
| /media | Mount point for removable media (USB, CD-ROM). | Auto-mounted external devices |



TYPES OF FILE SYSTEM 
-


| File System | Category | Description | Key Features | Used In |
|-------------|----------|-------------|--------------|----------|
| ext2 | Linux | Second Extended File System | No journaling | Older Linux systems |
| ext3 | Linux | Enhanced version of ext2 with journaling | Journaling support | Stable Linux environments |
| ext4 | Linux | Fourth Extended File System | Faster, supports large files, journaling | Default in most Linux distributions |
| XFS | Linux | High-performance journaling file system | Excellent for large data, parallel I/O | Servers & enterprise storage |
| Btrfs | Linux | Modern copy-on-write file system | Snapshots, compression, self-healing | Advanced Linux setups |
| ZFS | Unix/Linux | Advanced file system + volume manager | Data integrity, RAID, snapshots | Enterprise storage systems |


