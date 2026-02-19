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
   

3. Command Substitution Variable - Stores output of a command.

                   current_user=$(whoami)
                   today=$(date)


4. Local Variables: Inside function only.

               function greet() {
               local name="Swetha"
               echo $name
                            }
   

5. Global Variable - Accessible everywhere.

              name="Swetha"

6. Environment or System Variables - Predefined system variables.

Example:

            echo $HOME - User home directory
            echo $USER - Current user
            echo $PATH - Executable search path
            echo $PWD  - Present working directory
            echo $SHELL - Current shell
            echo $RANDOM - It gives any random Numbers
            echo &SECONDS - The number of seconds the Scripts Started 
            echo &LINENO - Returns the current line number in bash scripts
            

7. Exporting Variables - If you want a variable available to child processes:

           export project=DevOps

8. read Input from User
   
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
