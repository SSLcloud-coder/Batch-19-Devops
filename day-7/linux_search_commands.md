
# 📘 Linux Search Commands (`grep`, `find`, `locate`)

---

## 🔹 **1. `grep` Command**

### 📖 **Definition**
`grep` stands for **Global Regular Expression Print**.  
It is used to **search text patterns inside files** and print matching lines.

---

### ⚙️ **Syntax**
```bash
grep [options] "pattern" filename
```

---

### 🛠️ **Common Options**

| Option | Description | Example |
|--------|-------------|---------|
| `-i`   | Ignore case (case-insensitive search) | `grep -i "linux" file.txt` |
| `-n`   | Show line numbers with matches | `grep -n "error" logfile.log` |
| `-c`   | Show only the count of matches | `grep -c "fail" logfile.log` |
| `-v`   | Show lines that **do not** match | `grep -v "root" /etc/passwd` |
| `-w`   | Match whole word only | `grep -w "cat" animals.txt` |
| `-r`   | Search recursively in directories | `grep -r "TODO" /home/user` |
| `-l`   | Show only filenames with matches | `grep -l "main" *.c` |
| `-L`   | Show only filenames **without** matches | `grep -L "main" *.c` |
| `-o`   | Show only the matching text (not the whole line) | `grep -o "192.168.*" config.txt` |
| `-e`   | Search multiple patterns | `grep -e "error" -e "fail" logfile.log` |
| `-A n` | Show n lines **after** match | `grep -A 2 "error" logfile.log` |
| `-B n` | Show n lines **before** match | `grep -B 2 "error" logfile.log` |
| `-C n` | Show n lines before & after match | `grep -C 3 "error" logfile.log` |

---

### ✅ **Examples**
```bash
grep "root" /etc/passwd  
grep -i "linux" os.txt  
grep -c "404" access.log  
grep -v "sonu" students.txt  
grep -r "main" /home/projects  
grep -n "bash" /etc/passwd  
```

---

## 🔹 **2. `find` Command**

### 📖 **Definition**
`find` is used to **search files and directories** based on name, type, size, owner, permissions, or modification time.

---

### ⚙️ **Syntax**
```bash
find [path] [options] [expression]
```

---

### 🛠️ **Common Options**

| Option | Description | Example |
|--------|-------------|---------|
| `-name`   | Search by name (case-sensitive) | `find /home -name "file.txt"` |
| `-iname`  | Search by name (case-insensitive) | `find /home -iname "file.txt"` |
| `-type`   | Search by type (`f`=file, `d`=dir, `l`=link) | `find /etc -type d` |
| `-size`   | Search by file size (`+` greater, `-` smaller) | `find / -size +100M` |
| `-user`   | Search files owned by a user | `find /var -user root` |
| `-group`  | Search by group | `find /home -group dev` |
| `-perm`   | Search by permissions | `find /etc -perm 644` |
| `-mtime`  | Modified in last n days | `find /var/log -mtime -2` |
| `-atime`  | Accessed in last n days | `find /home -atime +10` |
| `-ctime`  | Changed status in last n days | `find /etc -ctime 1` |
| `-empty`  | Find empty files or directories | `find /tmp -empty` |
| `-exec`   | Run a command on found files | `find / -name "*.log" -exec rm {} \;` |
| `-maxdepth n` | Limit search depth | `find /home -maxdepth 1 -name "*.txt"` |
| `-mindepth n` | Start search after certain depth | `find / -mindepth 2 -name "*.sh"` |
| `-newer file` | Find files newer than another file | `find . -newer file1.txt` |

---

### ✅ **Examples**
```bash
find /home -name "notes.txt"  
find /home -iname "notes.txt"  
find /etc -type d  
find / -size +100M  
find /var -user root  
find /var/log -mtime -2  
find /tmp -empty  
find /home -name "*.tmp" -exec rm -f {} \;  
find /home -maxdepth 1 -name "*.sh"  
```

---

## 🔹 **3. `locate` Command**

### 📖 **Definition**
`locate` is used to **quickly find files** using a pre-built database (`mlocate.db`).  
It is much faster than `find` but may not always be up-to-date (you need to run `updatedb`).

---

### ⚙️ **Syntax**
```bash
locate [options] pattern
```

---

### 🛠️ **Common Options**

| Option | Description | Example |
|--------|-------------|---------|
| No option | Simple file search | `locate file.txt` |
| `-i`   | Case-insensitive search | `locate -i notes.txt` |
| `-n N` | Show only N results | `locate -n 5 file.txt` |
| `-c`   | Show only the count of results | `locate -c file.txt` |
| `-r`   | Use regex pattern | `locate -r '\.log$'` |
| `-e`   | Check file existence | `locate -e oldfile.txt` |

---

### ✅ **Examples**
```bash
locate file.txt  
locate -i readme.md  
locate -n 5 passwd  
locate -c ssh  
locate -r '\.log$'  
sudo updatedb  
```

---

## 🎯 **Difference Between `grep`, `find`, and `locate`**

| Command | Works On | Best Used For | Example |
|---------|----------|---------------|---------|
| `grep`  | **File content** | Search inside text files | `grep "error" logfile.log` |
| `find`  | **Filesystem (metadata)** | Search files by name, size, owner, etc. | `find /home -name file.txt` |
| `locate`| **Database (`mlocate.db`)** | Very fast filename search | `locate file.txt` |
