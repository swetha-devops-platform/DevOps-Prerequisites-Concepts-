Filters and I/O Redirection in Linux
-

## Filters in Linux

Filters are commands that:

- Take input from **Standard Input (stdin)**
  
- Process the data
  
- Produce output to **Standard Output (stdout)**

Filters are commonly used with pipes (`|`).

### Common Filter Commands

| Command | Purpose | Example |
|----------|----------|----------|
| `cat` | Display file content | `cat file.txt` |
| `grep` | Search for pattern | `grep "error" file.txt` |
| `sort` | Sort lines | `sort file.txt` |
| `uniq` | Remove duplicate lines | `uniq file.txt` |
| `wc` | Count lines, words, characters | `wc -l file.txt` |
| `head` | Show first 10 lines | `head file.txt` |
| `tail` | Show last 10 lines | `tail file.txt` |
| `cut` | Extract columns | `cut -d":" -f1 /etc/passwd` |
| `tr` | Translate characters | `tr a-z A-Z` |

---

### Pipe Operator

`|` is used to connect multiple commands.

Handson Commands: 

- grep command:

<img width="1398" height="364" alt="image" src="https://github.com/user-attachments/assets/74c90998-f922-4fb6-ad7f-89ccf3560f59" />

- grep -i command : This command will Ignore the Case senstivie 

<img width="1152" height="311" alt="image" src="https://github.com/user-attachments/assets/bc3a5f8b-07e8-43db-9c5f-e1b0b19ba18b" />

- grep -iR * Command : This command is used to filter the words in directory and files also

<img width="894" height="386" alt="image" src="https://github.com/user-attachments/assets/07bead97-b618-46ab-9631-05c6e627c428" />


This sends output of `cat` as input to `grep`.


Redirection in Linux
-

- Redirection in Linux is used to change the default input or output of a command.

- Normally:

  - Keyboard → Input

  - Screen → Output

- With redirection, we can:

  - Send output to a file

  - Take input from a file

  - Append output

  - Handle error messages

##  I/O Redirection in Linux

Linux has 3 standard streams:

| Stream | Number | Description |
|--------|--------|------------|
| Standard Input | 0 | Input (keyboard) |
| Standard Output | 1 | Normal output |
| Standard Error | 2 | Error messages |

---

## Types of Redirection 

| Type | Symbol | Description | Example | Notes |
|------|--------|-------------|----------|-------|
| Output Redirection | > | Sends output to a file (overwrites existing content) | echo "Hello Swetha" > file.txt | Creates file if not exists, overwrites content |
| Append Output | >> | Appends output to end of file | echo "DevOps Learning" >> file.txt | Does not remove old content |
| Input Redirection | < | Takes input from a file instead of keyboard | cat < file.txt | Reads input from file |
| Error Redirection | 2> | Redirects error messages to a file | ls wrongfile 2> error.txt | Stores only error output |
| Redirect Output & Error | > file 2>&1 | Redirects both normal output and error | ls file1 wrongfile > output.txt 2>&1 | Stores both output and error in same file |
| Pipe | \| | Sends output of one command to another command | ls -l \| grep .txt | Used heavily in DevOps scripting |

### Redirection Operators

| Operator | Purpose | Example |
|----------|----------|----------|
| `>` | Redirect output (overwrite) | `ls > file.txt` |
| `>>` | Append output | `ls >> file.txt` |
| `<` | Take input from file | `wc -l < file.txt` |
| `2>` | Redirect error | `ls wrongfile 2> error.txt` |
| `&>` | Redirect both output & error | `command &> file.txt` |


Handson of redirection Commands: 

- Output Redirection - >


<img width="599" height="130" alt="image" src="https://github.com/user-attachments/assets/303d454d-8a50-4f11-ad2a-3fcd763f4815" />


- Append Output -  >>

<img width="597" height="110" alt="image" src="https://github.com/user-attachments/assets/4e8ca515-e7a4-4ea2-895f-40a5a48c8716" />







