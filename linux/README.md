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



## Day 6: Sudo, Root User and File Ownership

### Objective
Understand administrator privileges, the root user, and file ownership in Linux.

### Commands Practiced

| Command | Purpose |
|---|---|
| `sudo -l` | Lists commands permitted through sudo |
| `sudo whoami` | Displays `root` when run with root privileges |
| `whoami` | Displays the current user identity |
| `ls -l practice/test.txt` | Displays file permissions, owner, and group |
| `id` | Displays user ID, group ID, and group memberships |

### Key Concepts

- **Sudo:** Allows an authorized user to execute commands with elevated privileges.
- **Root user:** The Linux administrator account with extensive system-wide access.
- **File ownership:** Every file has an owner and an associated group.
- **Chown:** A command used to change file ownership.

### Practical Work
Checked sudo permissions, compared `whoami` with `sudo whoami`, and inspected file ownership using `ls -l`.

### Key Learnings
I learned how Linux separates normal user activity from administrative tasks and how ownership information helps manage access to files.

### Cloud Computing Application
Sudo and ownership management are important when administering cloud servers, installing software, maintaining configurations, and protecting system resources.

---

### Progress Summary

- **Day 4:** Viewing and searching files
- **Day 5:** Users, groups, and permissions
- **Day 6:** Sudo, root user, and file ownership

**Next:** Day 7 — Linux processes, CPU usage, and memory monitoring.




## Day 7: Processes, CPU and Memory

### Topics Learned
- Understanding Linux processes and Process IDs (PIDs)
- Viewing processes using `ps` and `ps aux`
- Understanding CPU and memory usage
- Checking RAM and swap memory with `free -h`
- Checking system uptime and load average with `uptime`

### Commands Practised

```bash
ps
ps aux
free -h
uptime
```

### Key Learnings
- A process is a running program.
- Each process has a unique PID.
- RAM is temporary working memory, while SSD or hard drive storage retains files.
- Linux provides commands to inspect memory usage and system workload.
- These commands are useful for basic Linux and cloud-server monitoring.

### Practical Work
Executed the commands in Ubuntu on WSL and observed running processes, memory statistics, swap usage, uptime, and load averages.

### Outcome
Learned the basics of Linux process monitoring and system resource inspection.


## Day 8: Linux Networking Basics

### Topics Learned
- Network interfaces and IP addresses
- Testing connectivity using `ping`
- Understanding hostnames
- DNS name resolution
- Gateways and routing tables

### Commands Practised

```bash
ip a
ping -c 4 google.com
hostname
getent hosts google.com
ip route
```

### Key Learnings
- `ip a` displays network interfaces and their IP addresses.
- `ping` checks whether a destination responds over the network.
- `hostname` displays the system's hostname.
- `getent hosts` looks up addresses associated with a domain name.
- `ip route` displays routes used to direct network traffic.
- A default route is used when no more specific route matches.

### Practical Work
Executed networking commands in Ubuntu on WSL and inspected network interfaces, connectivity, hostname, DNS results, and routing information.

### Outcome
Learned the basics of Linux networking and practised commands useful for understanding cloud-server connectivity.



## Day 9: Linux Networking and Troubleshooting

### Topics Learned
- Testing network reachability with `ping`
- Looking up domain addresses with `getent hosts`
- Checking website responses with `curl`
- Understanding HTTP status codes
- Checking command availability with `command -v`
- Viewing DNS configuration in `/etc/resolv.conf`

### Commands Practised

```bash
ping -c 4 github.com
getent hosts github.com
curl -I https://github.com
curl -s -o /dev/null -w "%{http_code}\n" https://github.com
command -v curl
command -v tracepath
cat /etc/resolv.conf
getent hosts microsoft.com
```

### Key Learnings
- `ping` checks whether a destination responds to network messages.
- `getent hosts` looks up addresses associated with domain names.
- `curl` can inspect a website's HTTP response.
- HTTP status code `200` indicates a successful request.
- `command -v` checks whether Linux can locate a command.
- `/etc/resolv.conf` contains DNS-related settings.

### Practical Work
Tested GitHub connectivity, looked up domain addresses, inspected HTTP response headers, checked command availability, and viewed DNS configuration in Ubuntu on WSL.

### Outcome
Practised introductory Linux networking troubleshooting commands.



## Day 10: Downloading and Inspecting Files

### What I Learned
Today, I learned how to download webpage content using `curl` and inspect the downloaded file using Linux commands.

### Commands Practiced

**1. Download webpage content**
```bash
curl -o hello.txt https://example.com
```
Downloads the webpage's content and saves it as `hello.txt`.

**2. Check file details**
```bash
ls -l hello.txt
```
Displays the file's size and other details.

**3. Display file contents**
```bash
cat hello.txt
```
Shows the downloaded HTML content.

**4. Count lines**
```bash
wc -l hello.txt
```
Counts the number of lines in the file.

**5. Count words**
```bash
wc -w hello.txt
```
Counts the words in the file.

**6. Check disk usage**
```bash
du -h hello.txt
```
Shows the disk space used by the file in a human-readable format.

**7. Identify the file type**
```bash
file hello.txt
```
Identifies the file as an HTML document containing ASCII text.

### Key Takeaways
- `curl` can download content from a website.
- `-o` saves the downloaded content to a file.
- HTML is the code used to structure webpages.
- `wc` counts lines and words.
- `du` checks disk space usage.
- `file` helps identify a file's type.

### Day 10 Summary
I practiced downloading webpage content and inspecting a file using Linux commands. These skills are useful for understanding files and working with internet resources in Linux and cloud environments.

