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


Concepts in Variable 

1. String Variable: - city="Chennai"


<img width="455" height="100" alt="image" src="https://github.com/user-attachments/assets/6710f0f2-fda7-41d4-ac1d-e565d1afa68f" />

   

2. Number Variable: - num=10


<img width="538" height="68" alt="image" src="https://github.com/user-attachments/assets/4d740db0-2f4a-46a5-8d36-5e624996183f" />



3. Command Substitution Variable - Command substitution means storing the output of a command inside a variable. Simple Terms : Run a command and capture its output.

   The two methods

        1. Modern: $(command) -  $( ) preferred over backticks - Because:  It is more readable, Supports nested commands, Easier to maintain


<img width="828" height="78" alt="image" src="https://github.com/user-attachments/assets/ef942907-980c-4848-b933-e1c4202ffcf2" />


        2. Old: `command` - ` this is not an Single quote. it is an battish


<img width="678" height="175" alt="image" src="https://github.com/user-attachments/assets/c4faf138-8d6a-43f1-a8dc-6e6c2542971e" />



4. Exporting Variables - 

            By default, a variable created in Bash is local to that shell session. If you want the variable to be available to: Child processes, Sub-shells Other scripts - You must export it. export converts a shell variable into an environment variable.

            For Every User - /etc/profile - Give the exported Variables in basharc
            
            For Praticular User - Give the Exported Variable in Basharc for the particular User

            Syntax : export VariableName=Value

There are two types of variables:

            Shell variable → Only available in current shell
   
            Environment variable → Available to child processes

                    echo $HOME - User home directory
                    echo $USER - Current user
                    echo $PATH - Executable search path
                    echo $PWD  - Present working directory
                    echo $SHELL - Current shell
                    echo $RANDOM - It gives any random Numbers
                    echo &SECONDS - The number of seconds the Scripts Started 
                    echo &LINENO - Returns the current line number in bash scripts


How to Check Exported Variables: 
          
             env or printenv - These commands show only exported (environment) variables.


Export Variables are Permantely saved in Root Directory hidden Files in the basharch files we should type our exported variables 


<img width="1295" height="117" alt="image" src="https://github.com/user-attachments/assets/8905d11e-6720-449c-a521-0e789b836e67" />



5. CommandLine Arugments (Very Important for DevOps 🔥) - Command line arguments are values passed to a script when executing it.
      

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

            

6. Quotes  - Quotes are used to control how Bash reads text.

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







           
