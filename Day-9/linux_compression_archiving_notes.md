
# Linux Compression and Archiving Commands – Full Notes

## 1. Introduction
In Linux, we often need to:
- **Archive files** (combine many files into one for easy storage/transfer).
- **Compress files** (reduce file size to save disk space).

👉 **Archiving** ≠ **Compression**.  
- Archiving = grouping files together.  
- Compression = reducing file size.  

Example:
- `tar` creates an archive (`.tar`).
- `gzip` compresses it (`.tar.gz`).

---

## 2. Archiving Commands

### 2.1 `tar` (tape archive)
Most common archiving tool in Linux.

**Syntax:**
```bash
tar [options] archive_name.tar file1 file2 ...
```

**Options:**
- `-c` → Create archive
- `-x` → Extract archive
- `-t` → List contents of archive
- `-v` → Verbose (show process)
- `-f` → File name of archive
- `-z` → Use gzip compression
- `-j` → Use bzip2 compression
- `-J` → Use xz compression
- `--remove-files` → Delete original files after archiving
- `--exclude=pattern` → Exclude files

**Examples:**

1. Create an archive:
```bash
tar -cvf backup.tar file1 file2 dir1
```

2. Extract an archive:
```bash
tar -xvf backup.tar
```

3. List contents without extracting:
```bash
tar -tvf backup.tar
```

4. Create tar with gzip compression:
```bash
tar -czvf backup.tar.gz dir1
```

5. Extract tar.gz file:
```bash
tar -xzvf backup.tar.gz
```

6. Exclude a file during archiving:
```bash
tar -czvf backup.tar.gz dir1 --exclude=dir1/file2
```

7. Append a file to existing archive:
```bash
tar -rvf backup.tar newfile.txt
```

---

## 3. Compression Commands

### 3.1 `gzip`
Compresses files (makes `.gz`).

**Syntax:**
```bash
gzip filename
```

**Examples:**

1. Compress a file:
```bash
gzip file1.txt
```

2. Decompress (unzip):
```bash
gunzip file1.txt.gz
```
or
```bash
gzip -d file1.txt.gz
```

3. Keep original file after compression:
```bash
gzip -c file1.txt > file1.txt.gz
```

---

### 3.2 `bzip2`
Better compression than gzip but slower.

**Examples:**

1. Compress file:
```bash
bzip2 file1.txt
```

2. Decompress:
```bash
bunzip2 file1.txt.bz2
```

---

### 3.3 `xz`
Very high compression ratio.

**Examples:**

1. Compress:
```bash
xz file1.txt
```

2. Decompress:
```bash
unxz file1.txt.xz
```

---

## 4. Other Useful Commands

### 4.1 `zip`
Cross-platform compression (Windows compatible).

**Examples:**

1. Create zip:
```bash
zip archive.zip file1 file2
```

2. Zip a directory:
```bash
zip -r archive.zip dir1
```

3. Unzip:
```bash
unzip archive.zip
```

---

### 4.2 `compress` (older tool)
Creates `.Z` files (rarely used).

**Example:**
```bash
compress file1.txt
```
(decompress with `uncompress file1.txt.Z`)

---

## 5. Comparison Table

| Command | Extension | Usage | Notes |
|---------|-----------|-------|-------|
| tar     | .tar      | Archiving only | Does not compress |
| gzip    | .gz       | Compression | Fast but less efficient |
| bzip2   | .bz2      | Compression | Slower but better compression |
| xz      | .xz       | Compression | Very high compression |
| zip     | .zip      | Archive + Compression | Cross-platform |
| compress| .Z        | Compression | Old, rarely used |

---

## 6. Practical Scenarios

1. **Backup directory with tar.gz**
```bash
tar -czvf backup_$(date +%F).tar.gz /home/user/
```

2. **Extract to specific directory**
```bash
tar -xzvf backup.tar.gz -C /tmp/extract_here
```

3. **Compress large log file with xz**
```bash
xz /var/log/messages
```

4. **Check archive size before transfer**
```bash
du -sh backup.tar.gz
```
