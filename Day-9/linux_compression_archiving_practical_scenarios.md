
# Linux Compression & Archiving – Practical Scenarios with Q&A

## 🔹 Scenario 1 – Backing Up a Directory
**Q:** You have a directory named `project` that you need to back up and compress into a single file. Which command will you use?  
**A:**  
```bash
tar -czvf project.tar.gz project
```
This creates `project.tar.gz` containing all files and subfolders.

---

## 🔹 Scenario 2 – Extracting Archived Files
**Q:** You received a file `data.tar.gz`. How do you restore its contents?  
**A:**  
```bash
tar -xzvf data.tar.gz
```
This extracts all files into the current directory.

---

## 🔹 Scenario 3 – Compressing a Single File
**Q:** You want to compress `report.txt` using **xz** but also keep the original file. Which command do you use?  
**A:**  
```bash
xz -k report.txt
```
This creates `report.txt.xz` and keeps `report.txt`.

---

## 🔹 Scenario 4 – Creating a Windows-Compatible Archive
**Q:** You want to share all `.pdf` files with a Windows user in one compressed file. Which command will you use?  
**A:**  
```bash
zip documents.zip *.pdf
```
This creates `documents.zip` containing all PDFs.

---

## 🔹 Scenario 5 – Viewing Archive Contents Without Extraction
**Q:** You want to check what files are stored inside `backup.tar.xz` without extracting them. What command do you use?  
**A:**  
```bash
tar -tJvf backup.tar.xz
```
This lists the files inside the archive.

---

## 🔹 Scenario 6 – Archiving Multiple Log Files
**Q:** You need to archive three logs (`sys.log`, `app.log`, `err.log`) into one compressed file using bzip2. Which command do you use?  
**A:**  
```bash
tar -cjvf logs.tar.bz2 sys.log app.log err.log
```
This creates a bzip2-compressed tarball.

---

## 🔹 Scenario 7 – Excluding Files During Archiving
**Q:** You want to create a compressed archive of `/home/user/` but exclude `temp.log`. Which command will you use?  
**A:**  
```bash
tar -czvf backup.tar.gz /home/user --exclude=temp.log
```
This archives everything except `temp.log`.

---

## 🔹 Scenario 8 – Extracting to a Specific Directory
**Q:** You have `backup.tar.gz` and want to extract it into `/tmp/test`. Which command do you use?  
**A:**  
```bash
tar -xzvf backup.tar.gz -C /tmp/test
```
This extracts files into `/tmp/test`.

---

## 🔹 Scenario 9 – Checking Compressed File Content Without Extracting
**Q:** You want to read a `.gz` file without extracting it. Which command do you use?  
**A:**  
```bash
zcat file.txt.gz
```
This shows the file content directly.

---

## 🔹 Scenario 10 – Old `compress` Tool
**Q:** How do you compress `data.txt` with the legacy **compress** tool?  
**A:**  
```bash
compress data.txt
```
This creates `data.txt.Z`.  

To decompress:  
```bash
uncompress data.txt.Z
```
