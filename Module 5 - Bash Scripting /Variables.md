Variable : 

        A variable in Bash is a named container used to store data like strings, numbers, or command output.
        Bash variables are dynamically typed (no need to declare data type).
        We use an " = " Sign to declare an Variable 

Declareing  a variable: 

name=Swetha
age=24
" Important - No spaces around = "

Accessing a variable: 

echo $name
Use $ symbol to access the value.


<img width="516" height="93" alt="image" src="https://github.com/user-attachments/assets/09646e70-66da-49e7-baf3-b74547caf6a8" />


Variable Types in Bash - Even though Bash has no strict data types, we use them like this:


1. String Variable:
   
                city="Chennai"
   

2. Number Variable:
   
                   num=10
   

3. Command Substitution Variable - Command substitution means storing the output of a command inside a variable. Simple Terms : Run a command and capture its output.

   The two methods

        1. Modern: $(command) -  $( ) preferred over backticks - Because:  It is more readable, Supports nested commands, Easier to maintain


<img width="828" height="78" alt="image" src="https://github.com/user-attachments/assets/ef942907-980c-4848-b933-e1c4202ffcf2" />


        2.Old: `command` - ` this is not an Single quote. it is an battish


<img width="678" height="175" alt="image" src="https://github.com/user-attachments/assets/c4faf138-8d6a-43f1-a8dc-6e6c2542971e" />



5. Local Variables: Inside function only.

               function greet() {
               local name="Swetha"
               echo $name
                            }
   

6. Global Variable - Accessible everywhere.

              name="Swetha"

7. Environment or System Variables - Predefined system variables.

Example:

            echo $HOME - User home directory
            echo $USER - Current user
            echo $PATH - Executable search path
            echo $PWD  - Present working directory
            echo $SHELL - Current shell
            echo $RANDOM - It gives any random Numbers
            echo &SECONDS - The number of seconds the Scripts Started 
            echo &LINENO - Returns the current line number in bash scripts
            

7. Exporting Variables - By default, a variable created in Bash is local to that shell session. If you want the variable to be available to: Child processes, Sub-shells Other scripts - You must export it.

            Syntax : export VariableName=Value

   There are two types of variables:

            Shell variable → Only available in current shell
   
            Environment variable → Available to child processes

export converts a shell variable into an environment variable.

How to Check Exported Variables: 
          
            env or printenv - These commands show only exported (environment) variables.


Export Variables are Permantely saved in Root Directory hidden Files 


<img width="1295" height="117" alt="image" src="https://github.com/user-attachments/assets/8905d11e-6720-449c-a521-0e789b836e67" />




9. read Input from User
   
            read name
            echo "Hello $name"

With message:
           read -p "Enter your name: " name
           

9. Default Values in Variables
    
           echo ${name:-"DefaultName"}
If name is empty → prints DefaultName.



10. Constant Variable (Readonly)
    
          readonly company="TCS"
          Cannot change later.


11. Arithmetic with Variables
    
          a=10
          b=5
          sum=$((a+b))
          echo $sum


CommandLine Arugments (Very Important for DevOps 🔥) - Command line arguments are values passed to a script when executing it.
      

            Variable	      Meaning

             $0	              Script name

             $1	              First argument

             $2	              Second argument

             $#	              Number of arguments

             $@	              All arguments( individually ) 

             $?	              Last command exit status

             $$	              Process ID

             $*               All arguments (as single string)

Example:

            ./script.sh Swetha DevOps

Inside script:

            echo $1   # Swetha
            echo $2   # DevOps

Quotes  - Quotes are used to control how Bash reads text.


Bash normally:

            Splits words by space

            Expands variables

            Executes special characters

Quotes tell Bash:

           “Treat this text in a special way.”


Bash does 3 main things automatically:

           Variable expansion → $name

          Command execution → $(date)

          Word splitting → Space separates words
          

Quotes control these behaviors.


Types of Quotes - Double Quotes & Single Quotes 


Double Quotes 

What it does:

           Allows variable expansion
 
           Allows command substitution

          Prevents word splitting (mostly)

<img width="690" height="69" alt="image" src="https://github.com/user-attachments/assets/6dd9916d-a55d-4909-a89c-c0215b132ace" />


Single Quotes 

What it does:

        Stops variable expansion

        Stops command execution

        Treats everything literally

<img width="586" height="107" alt="image" src="https://github.com/user-attachments/assets/acf7f48b-78f1-4874-a13f-5d2c5d35253a" />


To Print Special Characters we have to use an \ "Backward Slash " 


<img width="1009" height="54" alt="image" src="https://github.com/user-attachments/assets/eb546f8f-4dae-4f3a-8937-63fd606ce9c4" />


Command Substitution: 





           
