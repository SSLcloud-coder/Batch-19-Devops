# 🎯 Linux Commands Practice Set (Interview + Examples + Assignments)

---

## 🔹 1. `ls` – List files & directories
**Interview Q:** What does `ls` do?  
**Answer:** Lists files and directories.

✅ **Examples:**
```bash
ls          # simple listing
ls -l       # detailed list
ls -a       # hidden files
ls -lh      # human readable size
```

📌 **Assignment:**
- List hidden files in your home directory.  
- Get detailed listing of `/etc`.

---

## 🔹 2. `cd` – Change Directory
**Interview Q:** What is the purpose of `cd`?  
**Answer:** Changes the current working directory.

✅ **Examples:**
```bash
cd /etc
cd ~
cd ..
```

📌 **Assignment:**
- Go to `/var/log` and return to home.  
- Move two levels up using `cd ..`.

---

## 🔹 3. `pwd` – Print Working Directory
**Interview Q:** What does `pwd` show?  
**Answer:** Shows the absolute path of the present working directory.

✅ **Example:**
```bash
pwd
```

📌 **Assignment:**
- Run `pwd` after navigating to three different directories.

---

## 🔹 4. `id` – Show User Info
**Interview Q:** What does `id` display?  
**Answer:** Displays UID, GID, and groups of the user.

✅ **Examples:**
```bash
id
id root
```

📌 **Assignment:**
- Find your UID.  
- Check UID & GID of root.

---

## 🔹 5. `vi` – Text Editor
**Interview Q:** Difference between `vi` and `vim`?  
**Answer:** `vim` is the advanced version of `vi`.

✅ **Examples:**
```bash
vi file.txt   # edit file
# i → insert mode
# :w → save
# :q → quit
# :wq → save & quit
# :q! → force quit
```

📌 **Assignment:**
- Create `note.txt` and add 3 lines.  
- Edit a file and update content.

---

## 🔹 6. `cat` – Concatenate & View Files
**Interview Q:** Use of `cat`?  
**Answer:** To view, create, or merge files.

✅ **Examples:**
```bash
cat file.txt
cat file1 file2 > merged.txt
cat > new.txt   # create new file (Ctrl+D to save)
```

📌 **Assignment:**
- Merge two files into a new one.

---

## 🔹 7. `touch` – Create Empty File
**Interview Q:** What does `touch` do?  
**Answer:** Creates empty file and updates timestamp.

✅ **Examples:**
```bash
touch file1.txt
touch file{1..5}.txt
```

📌 **Assignment:**
- Create 5 empty files.  
- Update timestamp of an existing file.

---

## 🔹 8. `echo` – Print Text / Variables
**Interview Q:** What is `echo` used for?  
**Answer:** Prints text or variables.

✅ **Examples:**
```bash
echo "Hello SSL Cloud"
echo $USER
echo $PATH
```

📌 **Assignment:**
- Print your username.  
- Create a variable and display its value.

---

## 🔹 9. `cp` – Copy Files
**Interview Q:** Difference between `cp` and `mv`?  
**Answer:** `cp` copies, while `mv` moves/renames.

✅ **Examples:**
```bash
cp file.txt /tmp/
cp -r dir1/ dir2/
```

📌 **Assignment:**
- Copy a file to `/tmp`.  
- Copy a directory recursively.

---

## 🔹 10. `mv` – Move / Rename Files
**Interview Q:** What does `mv` do?  
**Answer:** Moves or renames files.

✅ **Examples:**
```bash
mv file1.txt file2.txt
mv file.txt /tmp/
```

📌 **Assignment:**
- Rename a file.  
- Move a directory.

---

## 🔹 11. `mkdir` – Make Directory
**Interview Q:** Purpose of `mkdir`?  
**Answer:** Creates new directories.

✅ **Examples:**
```bash
mkdir testdir
mkdir -p dir1/dir2/dir3   # nested directories
```

📌 **Assignment:**
- Create a folder named `project`.  
- Create nested folder path `/tmp/demo/logs`.

---

## 🔹 12. `rm` – Remove Files & Directories
**Interview Q:** What does `rm` do?  
**Answer:** Deletes files or directories.

✅ **Examples:**
```bash
rm file.txt
rm -i file.txt       # confirmation
rm -r dir1/          # directory remove
rm -rf dir1/         # force remove
```

📌 **Assignment:**
- Delete a file.  
- Forcefully delete a directory.

---

# 📝 Final Practice Assignment
1. `mkdir project && cd project`  
2. `touch file1 file2 file3`  
3. `echo "SSL Cloud" > file1`  
4. `cp file1 copy_file1`  
5. `mv file2 renamed_file2`  
6. `cat file1 copy_file1 > merged.txt`  
7. Run `ls -l` to check  
8. `rm merged.txt`  
9. Run `pwd` and `id`

