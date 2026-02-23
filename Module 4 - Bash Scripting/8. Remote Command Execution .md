What is Remote Command Execution?

     Running commands on another machine (remote server) from your local system.
     
     Instead of logging into each server manually, we automate using Bash.

Why It Is Important in DevOps?

     In real projects, you may need to:
     
             Check disk usage on 50 servers
             Restart services remotely
             Deploy code to multiple servers
             Check logs across environments
            Update packages in all machines
            
Doing manually = Error

Using Bash + SSH = ✅ Automation


Basic Requirement: 

To execute commands remotely:

       SSH access
       Username
       IP Address
       Password OR SSH Key

Method 1: Simple SSH Command (Basic Level)

Syntax

        ssh username@remote_ip "command"

Example:

<img width="876" height="112" alt="image" src="https://github.com/user-attachments/assets/fc9bedd0-f365-4906-bb05-96b122929cd0" />

This will log in and execute uptime command.

Important : If you don't use quotes:


Method 2 : Passwordless SSH (Best Practice)

          Typing password every time is not good for automation.

          So we use SSH Key-based authentication.

Step 1: Generate SSH Key

               ssh-keygen

It creates:

             id_rsa (private key)

             id_rsa.pub (public key)

Step 2: Copy Key to Remote Server.

            ssh-copy-id user@remote_ip

Now login without password:

            ssh user@remote_ip

            
