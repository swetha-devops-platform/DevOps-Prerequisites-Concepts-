 Vi Editor:
 ---

- vi (Visual Editor) is a command-line text editor used in Linux/Unix systems to create and edit files.

- It is lightweight

- Available in almost every Linux system by default

- Mainly used for editing configuration files and scripts


Vim stands for Vi Improved.
-

- Most modern systems use an improved version called vim (Vi Improved).

- It is an advanced version of the vi editor used in Linux/Unix systems for creating and editing text files.

-  Vim = More powerful + More features than vi

-  Mostly used in servers where GUI is not available
  

Why vi is Important in DevOps?
-

As a DevOps Engineer, you will use vi to:

 - Edit configuration files inside /etc

 - Modify scripts

 - Update Docker, Nginx, Apache configs

 - Troubleshoot production servers (where GUI is not available)

In real-time servers, GUI is not available, so vi is mandatory knowledge.

Modes of vi Editor (Very Important for Interview)
-

vi works in 3 main modes:

| Mode           | Purpose                                   |
|----------------|-------------------------------------------|
| Command Mode   | Default mode (for navigation & commands) |
| Insert Mode    | Used to type/edit content                 |
| Last Line Mode | Used for save, quit, search               |


Command Mode
-

- Default mode when you open vi

- Used for copy, paste, delete, navigation

Command mode Commands: 
-

Navigation Commands
-

| Command | Action |
|----------|--------|
| h | Move left |
| l | Move right |
| j | Move down |
| k | Move up |
| w | Move to next word |
| b | Move to previous word |
| 0 | Move to beginning of line |
| $ | Move to end of line |
| gg | Go to first line |
| G | Go to last line |
| :n | Go to line number (Example: :10) |

Delete Commands
-

| Command | Action |
|----------|--------|
| x | Delete character |
| dd | Delete entire line |
| dw | Delete word |
| d$ | Delete from cursor to end of line |
| d0 | Delete from cursor to beginning |



### Copy (Yank) & Paste

| Command | Action |
|----------|--------|
| yy | Copy (yank) line |
| yw | Copy word |
| p | Paste after cursor |
| P | Paste before cursor |


### Undo & Redo

| Command | Action |
|----------|--------|
| u | Undo |
| Ctrl + r | Redo |


### Search Commands

| Command | Action |
|----------|--------|
| /word | Search forward |
| ?word | Search backward |
| n | Next match |
| N | Previous match |


### Other Useful Commands

| Command | Action |
|----------|--------|
| r | Replace single character |
| cc | Change entire line |
| C | Change from cursor to end |
| . | Repeat last command |
| v | Enter visual mode |

    
Insert Mode
-

- Used to write or edit text.

- Press:

  - i → Insert before cursor

  - a → Insert after cursor

  - o → New line below

Press Esc to return to Command Mode.

### Insert Mode Commands

| Command | Action |
|----------|--------|
| i | Insert before cursor |
| I | Insert at beginning of line |
| a | Insert after cursor |
| A | Insert at end of line |
| o | Open new line below |
| O | Open new line above |
| s | Delete character and enter insert mode |
| S | Delete entire line and enter insert mode |




Last Line Mode
-

- Used for saving and quitting.

- Press : to enter this mode.

### Last Line Mode Commands

| Command | Action |
|----------|--------|
| :w | Save file |
| :q | Quit |
| :wq | Save and quit |
| :x | Save and quit (if changes made) |
| :q! | Force quit without saving |
| :w filename | Save file with new name |
| :set nu | Show line numbers |
| :set nonu | Hide line numbers |
| :/word | Search forward |
| :%s/old/new/g | Replace all occurrences in file |
| :%s/old/new/gc | Replace with confirmation |
| :!command | Run Linux command inside vim |

Press `Esc` then `:` to enter Last Line Mode.
