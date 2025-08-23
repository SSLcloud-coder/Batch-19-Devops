
# VIM Advance Operations  

---

## Types of Modes in Vim Editor

1. **Insert Mode** → Used to insert text into any file.  
2. **ESC Mode** → Used to perform different operations (copy, paste, delete, undo, redo, etc.).  
3. **Command or Colon Mode** → Used to run commands.  

**Example:**  
`:wq` → Save and quit  

---

## Vi and Vim Advance Operations

```bash
# cp /etc/passwd /root
# ls
# vim passwd
```

---

### Examples of Insert Mode

- `i` → Insert text **before** the cursor  
- `a` → Insert text **after** the cursor  
- `o` → Insert new line **below** the cursor  
- `Shift + o` → Insert new line **above** the cursor  

---

### Examples of ESC Mode

- `yy` → Copy one line (`nyy` to copy *n* lines)  
- `p` → Paste content  
- `dd` → Delete one line  
- `u` → Undo  
- `Ctrl + r` → Redo  
- `cc` → Cut & copy a line  
- `yw` → Copy a word  
- `dw` → Delete a word  
- `cw` → Cut & copy a word  
- `Shift + d` → Delete from cursor to end of line  
- `x` → Delete character (forward)  
- `Shift + x` → Delete character (backward)  
- `Shift + g` → Go to end of file  
- `gg` → Go to start of file  
- `0` → Go to beginning of line  
- `Shift + $` → Go to end of line  
- `b` → Move cursor **word by word backward**  
- `w` → Move cursor **word by word forward**  
- `/root` → Search a word (Press `n` for next, `Shift + n` for previous)  

---

### Examples of Command / Colon Mode

- `:set number` OR `:se nu` → Show line numbers  
- `:10` → Jump to line number 10  
- `:se nonu` → Remove line numbers  
- `:se ic` → Disable case sensitivity  
- `/ROOT` → Search without case sensitivity  
- `:se noic` → Enable case sensitivity again  
- `:nohl` → Remove highlighted search results  
- `:wq` OR `:x` → Save and quit  
- `:q!` → Quit without saving  

---

## Copy Lines from One File to Another

```bash
# vim passwd
5yy       # Copy 5 lines
:edit /report
p         # Paste content
:wq       # Save & quit

# cat /report
```

---

## Set Permanent Line Numbers in All Files

```bash
# vim ~/.vimrc
se nu
:wq
```

Now, line numbers will appear automatically in every file.  

---

## Search and Replace in Vim

```bash
# vim passwd

:%s/root/network/g       # Replace all "root" with "network"
:1s/network/root/g       # Replace only in line 1
:1,13s/network/root/gi   # Replace from line 1 to 13 (ignore case)
:%s/nologin/bash/gic     # Confirm before replace
:wq                      # Save & quit
```

---

## Using `sed` Command (Stream Editor)

```bash
lsblk | grep part | sed 's/part/partitions/'
lsblk | grep part | sed 's/part/partitions/g'
lsblk | sed -e 's/boot/booting/g' -e 's/SWAP/swap/g'
lsblk | sed 's/boot/booting/g;s/SWAP/swap/g'
```

### Replace in a File with `sed`
```bash
head /etc/passwd > /report
cat /report
sed 's/root/japan/g' /report        # Replace but not save
sed -i 's/root/japan/g' /report     # Replace & save permanently
sed -i 's/japan/root/g' /report     # Replace back
sed 's/root/japan/2' /report        # Replace 2nd occurrence only
sed '1,5s/root/japan/g' /report     # Replace from line 1 to 5
sed -i '1,5s/root/japan/g' /report  # Replace from 1 to 5 & save
sed -i '1,5s/root/japan/gi' /report # Replace ignoring case
```

**Example Output:**
```
japan:x:0:0:japan:/japan:/bin/bash
bin:x:1:1:bin:/bin:/sbin/nologin
daemon:x:2:2:daemon:/sbin:/sbin/nologin
...
```
