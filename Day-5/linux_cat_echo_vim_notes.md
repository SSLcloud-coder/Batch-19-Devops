
# 📘 Linux Notes – `cat`, `echo`, and `vi/vim` Commands

---

## 🔹 1. `cat` Command (Concatenate Command)

### 👉 Purpose:
- To **create**, **view**, **merge**, **copy**, and **append** files.

### 👉 Syntax:
```bash
cat [options] [file...]
```

### ✅ Examples:

1. **View file content**
```bash
cat file.txt
```

2. **Create a new file**
```bash
cat > newfile.txt
Hello World
This is Linux
CTRL+D   # Save & exit
```

3. **Append content to a file**
```bash
cat >> newfile.txt
Appended line
CTRL+D
```

4. **Merge multiple files**
```bash
cat file1.txt file2.txt > merged.txt
```

5. **Copy content from one file to another**
```bash
cat file1.txt > file2.txt
```

6. **Show line numbers**
```bash
cat -n file.txt
```

7. **Remove extra blank lines**
```bash
cat -s file.txt
```

8. **Show `$` at end of each line**
```bash
cat -E file.txt
```

### 📌 `cat` Options Summary:

| Option | Description |
|--------|-------------|
| `-n`   | Show line numbers |
| `-b`   | Show line numbers only for non-empty lines |
| `-s`   | Remove repeated blank lines |
| `-E`   | Show `$` at the end of each line |
| `-T`   | Show tabs as `^I` |
| `-A`   | Show all hidden characters |
| `--help` | Help menu |
| `--version` | Version info |

---

## 🔹 2. `echo` Command

### 👉 Purpose:
- Used to **display messages** or **write text into files**.

### 👉 Syntax:
```bash
echo [options] [string]
```

### ✅ Examples:

1. **Print a message**
```bash
echo "Hello Linux"
```

2. **Print variables**
```bash
name="Sonu"
echo "My name is $name"
```

3. **Create a file using echo**
```bash
echo "This is a test file" > file.txt
```

4. **Append to an existing file**
```bash
echo "Another line added" >> file.txt
```

5. **Print with escape sequences**
```bash
echo -e "Line1\nLine2\nLine3"
```

6. **Disable new line**
```bash
echo -n "Hello"
echo " World"
```

### 📌 `echo` Options Summary:

| Option | Description |
|--------|-------------|
| `-e`   | Enable escape characters (like `\n`, `\t`) |
| `-n`   | Do not print a new line at the end |
| `--help` | Show help menu |

---

## 🔹 3. `vi` and `vim` Editor

### 👉 Difference:
- **vi** = Basic editor (default in Linux)  
- **vim** = Vi Improved (extra features like syntax highlighting, plugins, undo/redo)

### 👉 Start:
```bash
vi filename
vim filename
```

### ✅ Modes in vi/vim:
1. **Command Mode** → default (navigation, delete, copy, etc.)
2. **Insert Mode** → type text (`i`, `a`, `o`)
3. **Last Line Mode** → `:` commands (save, quit, search, replace)

### ✅ File Save and Exit:

| Command | Description |
|---------|-------------|
| `:w` | Save file |
| `:q` | Quit |
| `:wq` | Save & quit |
| `:q!` | Quit without saving |
| `:x` | Save & quit (shortcut) |

### ✅ Navigation:

| Command | Description |
|---------|-------------|
| `h` | Left |
| `l` | Right |
| `k` | Up |
| `j` | Down |
| `0` | Start of line |
| `$` | End of line |
| `w` | Next word |
| `b` | Previous word |
| `gg` | Go to top |
| `G` | Go to bottom |
| `:n` | Go to line number n (e.g. `:10`) |

### ✅ Editing:

| Command | Description |
|---------|-------------|
| `i` | Insert before cursor |
| `a` | Append after cursor |
| `o` | New line below |
| `O` | New line above |
| `r` | Replace one char |
| `R` | Replace mode |

### ✅ Delete:

| Command | Description |
|---------|-------------|
| `x` | Delete character |
| `dw` | Delete word |
| `dd` | Delete line |
| `d$` | Delete till end of line |
| `d0` | Delete till start of line |
| `dG` | Delete till end of file |

### ✅ Copy & Paste:

| Command | Description |
|---------|-------------|
| `yy` | Copy line |
| `nyy` | Copy n lines |
| `yw` | Copy word |
| `y$` | Copy till end of line |
| `p` | Paste after |
| `P` | Paste before |

### ✅ Undo & Redo:

| Command | Description |
|---------|-------------|
| `u` | Undo |
| `U` | Undo whole line |
| `CTRL+R` | Redo |

### ✅ Search & Replace:

| Command | Description |
|---------|-------------|
| `/word` | Search forward |
| `?word` | Search backward |
| `n` | Next match |
| `N` | Previous match |
| `:%s/old/new/g` | Replace all in file |
| `:s/old/new/g` | Replace in current line |

### ✅ Useful Settings:

| Command | Description |
|---------|-------------|
| `:set number` | Show line numbers |
| `:set nonumber` | Hide line numbers |
| `:set ignorecase` | Case insensitive search |
| `:syntax on` | Syntax highlighting |
| `:syntax off` | Disable highlighting |

---

# 📌 Final Recap

- **`cat`** → View, create, append, merge, copy files  
- **`echo`** → Display text, create/append files, show variables  
- **`vi/vim`** → Powerful text editors for creating & editing configuration files  
