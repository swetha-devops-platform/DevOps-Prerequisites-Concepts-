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


Variable Types in Bash

Even though Bash has no strict data types, we use them like this:

🔹 1. String Variable
city="Chennai"

🔹 2. Number Variable
num=10

🔹 3. Command Substitution Variable

Stores output of a command.

current_user=$(whoami)
today=$(date)

5️⃣ Local vs Global Variables
🔹 Local Variable

Inside function only.

function greet() {
    local name="Swetha"
    echo $name
}

🔹 Global Variable

Accessible everywhere.

name="Swetha"

6️⃣ Environment Variables 🌍

Predefined system variables.

Example:
echo $HOME
echo $USER
echo $PATH
echo $PWD

Common Environment Variables
Variable	Meaning
$HOME	User home directory
$USER	Current user
$PATH	Executable search path
$PWD	Present working directory
$SHELL	Current shell
7️⃣ Exporting Variables

If you want a variable available to child processes:

export project=DevOps


Now child scripts can use it.

8️⃣ Read Input from User
read name
echo "Hello $name"


With message:

read -p "Enter your name: " name

9️⃣ Special Variables (Very Important for DevOps 🔥)
Variable	Meaning
$0	Script name
$1	First argument
$2	Second argument
$#	Number of arguments
$@	All arguments
$?	Last command exit status
$$	Process ID
Example:
./script.sh Swetha DevOps


Inside script:

echo $1   # Swetha
echo $2   # DevOps

🔟 Default Values in Variables
echo ${name:-"DefaultName"}


If name is empty → prints DefaultName.

1️⃣1️⃣ Constant Variable (Readonly)
readonly company="TCS"


Cannot change later.

1️⃣2️⃣ Arithmetic with Variables
a=10
b=5
sum=$((a+b))
echo $sum
