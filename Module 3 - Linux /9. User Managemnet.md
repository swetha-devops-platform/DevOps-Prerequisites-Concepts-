# What are Users in Linux?

A **User** is an account that can log in and access the Linux system.

Each user has:

* Username
* User ID (UID)
* Home directory
* Default shell

##  Types of Users in Linux

| User Type | UID Range | GID | Home Directory | Default Shell | Purpose |
|------------|------------|------|----------------|---------------|----------|
| Root User | 0 | 0 | /root | /bin/bash (or /bin/sh) | Superuser with full system access |
| System Users | 1 – 999 (varies by distro) | System group ID | /nonexistent or /var/lib/service | /sbin/nologin or /bin/false | Used by system services (nginx, mysql, apache) |
| Normal Users | 1000 and above | Usually same as username | /home/username | /bin/bash | Regular human users who log into the system |


<img width="622" height="88" alt="image" src="https://github.com/user-attachments/assets/2b0a19e7-5dea-4ea9-ab86-0a98cfe80350" />


---

###  Root User

* UID = 0
  
* Full control over system
  
* Can install, delete, modify anything

Be careful while using root.

### System Users

* Created for services
  
* Usually cannot login
  
* Used by daemons (background processes)

Example:

* nginx
* apache
* mysql


### Normal Users

* Created for human users
  
* Limited permissions
  
* Has home directory like `/home/swetha`

- Adding User - [ useradd ] Command is used to add an user


<img width="660" height="70" alt="image" src="https://github.com/user-attachments/assets/3564ebfd-efaa-49dd-a96e-78668abd1a0c" />

Here id Command is used to print the id of the users and groups 




# What are Groups in Linux?

A **Group** is a collection of users.

- Groups are used to:

  * Manage permissions easily
    
  * Control access to files & directories
    
  * Improve security

Instead of giving permission to each user, we assign permission to a group.

---

## 🔹 Types of Groups

| Type            | Description                       |
| --------------- | --------------------------------- |
| Primary Group   | Default group assigned to user    |
| Secondary Group | Additional groups user belongs to |

---

### Example:

If Swetha is in `devops` group:

All users in `devops` group can access shared project files.

---

# Where User & Group Info is Stored?

| File        | Purpose                    |
| ----------- | -------------------------- |
| /etc/passwd | Stores user details        |
| /etc/shadow | Stores encrypted passwords |
| /etc/group  | Stores group details       |

---

# Important Commands

| Command                | Purpose                   |
| ---------------------- | ------------------------- |
| useradd username       | Create new user           |
| passwd username        | Set password              |
| userdel username       | Delete user               |
| groupadd groupname     | Create group              |
| usermod -aG group user | Add user to group         |
| id username            | Show user ID & group info |
| whoami                 | Show current user         |



