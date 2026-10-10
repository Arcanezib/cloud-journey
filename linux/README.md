Day 1 — Linux Command Line Basics

Today I started practicing Linux using Ubuntu on WSL.

Commands I learned pwd — shows my current location. ls — shows files and folders. mkdir — creates a new folder. cd — moves into a folder. cd .. — moves back to the previous folder. Practice

I created a folder named practice, entered it using cd practice, checked my location using pwd, and returned to my home folder using cd ...

What I understood

Linux uses the terminal to interact with the operating system using commands. I practiced basic navigation and folder management commands.

Next Step

Continue learning Linux file and directory commands.


## Day 2 — Linux File and Directory Operations

Today I practiced working with files and directories using the Linux terminal.

### Commands I learned

- `touch` — creates an empty file.
- `cat` — displays the contents of a file.
- `echo` — displays text.
- `>` — redirects text into a file.
- `cp` — copies a file.
- `mv` — renames or moves a file.
- `rm` — removes a file.
- `mkdir` — creates a directory.
- `ls` — lists files and directories.
- `cd` — changes the current directory.
- `cd ..` — moves to the parent directory.
- `pwd` — shows the current working directory.

### Practice

I created files using `touch`, added text to a file using `echo` and `>`, and viewed the contents using `cat`.

I also practiced copying a file using `cp`, renaming a file using `mv`, and deleting a file using `rm`.

I created a `practice` directory and created `test.txt` inside it. I then practiced moving between the home directory and the `practice` directory using `cd` and `cd ..`.

### What I understood

I learned the difference between files and directories and how directories can contain files.

I also learned how basic Linux file and directory operations are performed using the terminal.

### Next Step

Continue learning more Linux commands and file operations.



## Day 3 — Copying, Moving and Wildcards

Today I practiced more Linux file and directory operations.

### Commands I learned

- `cp` — copies files.
- `mv` — moves or renames files.
- `rm` — removes files.
- `mkdir` — creates a directory.
- `*` — wildcard used to match multiple files.
- `*.txt` — matches files ending with `.txt`.

### Practice

I copied `mybackup.txt` into the `practice` directory using `cp`.

I then moved `mybackup.txt` into the `practice` directory using `mv`.

I created a `backup` directory and copied all `.txt` files from the `practice` directory into it using:

`cp practice/*.txt backup/`

### What I understood

I learned the difference between `cp` and `mv`.

`cp` creates a copy while keeping the original file, whereas `mv` moves the file from one location to another.

I also learned how wildcards can be used to work with multiple files.

### Mistake and Learning

I initially used a space between `*` and `.txt`, which caused an error.

I learned that `*.txt` must be written together because it represents files ending with `.txt`.

### Next Step

Continue learning Linux commands for viewing and searching file contents.



## Day 4: Viewing and Searching Files

### Objective
Learn how to display file contents and search for specific text using Linux commands.

### Commands Practiced

| Command | Purpose |
|---|---|
| `cat practice/test.txt` | Displays the complete file contents |
| `head practice/test.txt` | Displays the first 10 lines by default |
| `tail practice/test.txt` | Displays the last 10 lines by default |
| `grep "Line 3" practice/test.txt` | Searches for specific text |
| `grep -i "line 3" practice/test.txt` | Searches without case sensitivity |
| `grep -n "Line 3" practice/test.txt` | Displays matching text with its line number |

### Practical Work
Created a five-line text file and practiced displaying its contents, viewing the beginning and end of the file, and searching for a specific line.

### Key Learnings
- `cat` displays file contents.
- `head` and `tail` show the beginning and end of a file.
- `grep` searches for text.
- The `-i` option ignores case differences.
- The `-n` option displays matching line numbers.

### Cloud Computing Application
These commands are useful for inspecting configuration files and searching application or server logs for relevant information.

---

## Day 5: Linux Users, Groups and Permissions

### Objective
Understand Linux users, groups, file permissions, and basic permission management.

### Commands Practiced

| Command | Purpose |
|---|---|
| `whoami` | Displays the current username |
| `id` | Displays user ID, group ID, and group information |
| `groups` | Lists the current user's groups |
| `ls -l practice/test.txt` | Displays detailed file information and permissions |
| `ls -ld practice` | Displays detailed information about the directory itself |
| `chmod u-w practice/test.txt` | Removes write permission for the owner |
| `chmod u+w practice/test.txt` | Restores write permission for the owner |

### Understanding Permissions

Linux uses three basic permissions:

- `r` — Read
- `w` — Write
- `x` — Execute

These permissions apply to the owner (`u`), group (`g`), and others (`o`).

For example, `-rw-r--r--` indicates a regular file where the owner can read and write, while the group and others can read it.

The `chmod` command changes permissions. I practiced removing and restoring the owner's write permission on a test file and verified the changes using `ls -l`.

### Key Learnings
- Linux identifies users and manages group memberships.
- File and directory permissions control access.
- `ls -l` helps inspect file permissions.
- `chmod` can add or remove permissions.

### Cloud Computing Application
Permissions help secure files, application configurations, and other resources on Linux cloud servers by controlling who can access or modify them.

---

## Progress Summary

- **Day 4:** Practiced viewing and searching files.
- **Day 5:** Practiced checking users, groups, and file permissions.
- **Next:** Learn about `sudo`, administrator privileges, and file ownership.
