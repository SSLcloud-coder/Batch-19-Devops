# Linux Basic Commands – Full Notes

## 1. Basic Linux Commands

| Command   | Description | Example | Output/Explanation |
|-----------|-------------|---------|--------------------|
| **`ls`**  | Lists files & directories in the current location | `ls` | Shows file & folder names |
|           | Show with details | `ls -l` | Long listing format |
|           | Show hidden files | `ls -a` | Includes `.hidden` files |
| **`date`** | Displays current system date & time | `date` | e.g., `Mon Aug 11 11:05:00 IST 2025` |
|           | Custom format | `date "+%d-%m-%Y"` | `11-08-2025` |
| **`cal`** | Shows calendar of the current month | `cal` | Calendar output |
|           | Show full year calendar | `cal 2025` | 12-month view |
| **`pwd`** | Shows **Present Working Directory** | `pwd` | e.g., `/home/user` |
| **`cd`**  | Change directory | `cd /etc` | Moves to `/etc` |
|           | Go to home directory | `cd` | Home folder |
|           | Go one step back | `cd ..` | Parent directory |
| **`whoami`** | Displays the current logged-in username | `whoami` | e.g., `root` |
| **`last`**   | Shows the last logged-in users with date & time | `last` | Login history from `/var/log/wtmp` |
|             | Show specific user’s login history | `last username` | Filtered login history |
| **`top`**    | Displays real-time system resource usage | `top` | CPU, memory, process usage |
|             | Show full command name in top output | Press `c` inside `top` | Full command path |

---

## 2. Absolute Path in Linux

- **Definition:** A full path starting from root `/`.
- Always starts with `/`.
- Works from any location.

**Example:**
```bash
cd /var/log
pwd
# Output: /var/log
```

---

## 3. Linux Command Structure

```bash
command  [argument]  [value]
```
- **Command** → Main action (`ls`, `cd`, `whoami`)
- **Argument** → Option (`-l`, `-a`, `-n`)
- **Value** → Target (`/etc`, `username`)

**Example:**
```bash
ls -l /home
# command: ls
# argument: -l
# value: /home
```

---

## 4. Help Commands in Linux

| Command | Purpose | Example | Output |
|---------|---------|---------|--------|
| **`man`** | Shows detailed manual page of a command | `man ls` | Opens full documentation |
| **`--help`** | Displays quick help & options | `ls --help` | List of flags & usage |
| **`info`** | Shows detailed info page | `info ls` | GNU info format |
| **`whatis`** | One-line description | `whatis pwd` | Short definition |
| **`apropos`** | Search commands related to keyword | `apropos calendar` | Related commands list |

---

### Using the `man` Command

**Syntax:**
```bash
man [section] command
```

**Sections in `man` pages**:
1 → User commands  
2 → System calls  
3 → Library functions  
4 → Special files  
5 → File formats  
6 → Games  
7 → Miscellaneous  
8 → System administration commands  

**Examples:**
```bash
man ls        # Show manual for ls
man 5 passwd  # Show /etc/passwd file format
```

**Navigation inside `man`:**
- **Space** → Scroll down
- **b** → Scroll up
- **q** → Quit
