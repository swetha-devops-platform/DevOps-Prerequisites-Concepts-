LINUX FILE SYSTEM :
-------
- The Linux File System is the way Linux organizes, stores, and manages files and directories.

- In Linux:

   - Everything is treated as a file - Regular files, Directories, Devices, Processes

   - Files are organized in a hierarchical structure

   - It starts from a single root directory → /

- Unlike Windows (C:, D: drives), Linux has one single tree structure.


 <img width="728" height="590" alt="image" src="https://github.com/user-attachments/assets/c7d6f7db-5a2c-4ad7-9f27-0df1f54be271" />


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


