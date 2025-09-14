# 📘 Linux Command Notes: `grep`, `cut`, `awk`

------------------------------------------------------------------------

## 🔍 1. `grep` Command

**Definition:**\
`grep` is used to **search text** or **patterns** inside files or
command outputs using **regular expressions**.

**Syntax:**

``` bash
grep [OPTIONS] PATTERN [FILE...]
```

------------------------------------------------------------------------

### ✅ Common Options of `grep`

-   `-i` → Ignore case\
-   `-v` → Invert match (show lines that do NOT match)\
-   `-n` → Show line numbers\
-   `-c` → Count matching lines\
-   `-l` → Show filenames with matches\
-   `-r` or `-R` → Search recursively in directories\
-   `-w` → Match whole word\
-   `-A NUM` → Print NUM lines **after** match\
-   `-B NUM` → Print NUM lines **before** match\
-   `-C NUM` → Print NUM lines **around** match\
-   `-E` → Use extended regex

------------------------------------------------------------------------

### 🖊 Examples of `grep`

1.  **Search a word in a file**

``` bash
grep "error" /var/log/messages
```

🔎 Finds all lines with `error` in log file.

2.  **Case-insensitive search**

``` bash
grep -i "disk" /var/log/syslog
```

🔎 Matches `disk`, `Disk`, `DISK`.

3.  **Count matches**

``` bash
grep -c "fail" auth.log
```

🔎 Shows how many times `fail` appears.

4.  **Show line numbers of matches**

``` bash
grep -n "root" /etc/passwd
```

🔎 Tells where exactly `root` entry is.

5.  **Search recursively in directory**

``` bash
grep -r "TODO" /home/project/
```

🔎 Finds `TODO` comments in all project files.

------------------------------------------------------------------------

## ✂️ 2. `cut` Command

**Definition:**\
`cut` extracts specific **columns** or **characters** from text lines.

**Syntax:**

``` bash
cut [OPTIONS] [FILE...]
```

------------------------------------------------------------------------

### ✅ Common Options of `cut`

-   `-c LIST` → Select specific characters (by position)\
-   `-f LIST` → Select specific fields (columns)\
-   `-d DELIM` → Define delimiter (default = TAB)\
-   `--complement` → Show all except selected fields

------------------------------------------------------------------------

### 🖊 Examples of `cut`

1.  **Extract first 10 characters**

``` bash
cut -c 1-10 filename.txt
```

🔎 Shows first 10 characters from each line.

2.  **Extract usernames from `/etc/passwd`**

``` bash
cut -d ":" -f1 /etc/passwd
```

🔎 Gets first field (`username`).

3.  **Get home directories from `/etc/passwd`**

``` bash
cut -d ":" -f6 /etc/passwd
```

🔎 Shows only home directory path.

4.  **Get multiple fields**

``` bash
cut -d ":" -f1,3,6 /etc/passwd
```

🔎 Extracts `username`, `UID`, `home directory`.

5.  **Remove one column and print rest**

``` bash
cut -d ":" --complement -f2 /etc/passwd
```

🔎 Prints all fields except 2nd (`password` placeholder).

------------------------------------------------------------------------

## 🪄 3. `awk` Command

**Definition:**\
`awk` is a **text processing tool** for extracting, filtering, and
performing operations on structured data.

**Syntax:**

``` bash
awk 'pattern { action }' [FILE]
```

------------------------------------------------------------------------

### ✅ Important Points

-   `$1, $2, ...` → Columns (fields)\
-   `$0` → Whole line\
-   `-F DELIM` → Define delimiter\
-   `NR` → Current line number\
-   `NF` → Number of fields in current line\
-   `BEGIN {}` → Runs before processing\
-   `END {}` → Runs after processing

------------------------------------------------------------------------

### 🖊 Examples of `awk`

1.  **Print first column (username)**

``` bash
awk -F ":" '{print $1}' /etc/passwd
```

2.  **Print username and home directory**

``` bash
awk -F ":" '{print $1, $6}' /etc/passwd
```

3.  **Show line numbers with output**

``` bash
awk '{print NR, $0}' file.txt
```

4.  **Condition: Print users with UID \> 1000**

``` bash
awk -F ":" '$3 > 1000 {print $1, $3}' /etc/passwd
```

5.  **Calculate sum of a column**

``` bash
awk '{sum += $2} END {print "Total:", sum}' sales.txt
```

(Assuming 2nd column has sales values)

------------------------------------------------------------------------

# 📌 Quick Comparison

  Command   Use Case
  --------- ----------------------------------------------
  `grep`    Search text/patterns in files
  `cut`     Extract specific characters/fields
  `awk`     Advanced filtering, formatting, calculations
