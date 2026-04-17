````md
# 🐧 Linux Basics - Class 01  
📅 **Date:** 30-03-2026  

![Linux](https://img.shields.io/badge/OS-Linux-blue?style=for-the-badge&logo=linux)
![Level](https://img.shields.io/badge/Level-Beginner-green?style=for-the-badge)
![Topic](https://img.shields.io/badge/Topic-CLI-important?style=for-the-badge)

---

## 📁 File Creation

```bash
touch <file_name> -----> To create the file_name
touch f1
touch f2 f3 f4
````

```bash
clear ----> To clean the screen
```

---

## 📂 Listing Files & Directories

```bash
ls -----> List all the files and directories
ls -l ---> List all the files and directories in the long format
ls -lt ---> List the files and directories based on the time
ls -lrt --> List the files in the reverse order
ls -lrth --> list the files in the reverse order with the size
```

---

## 📁 Directory Management

```bash
mkdir <directory_name> -----> To create the directory
mkdir sagar
mkdir test test1 test2
```

```bash
cd <directory_name> ----> To get into the directory
cd sagar
```

```bash
cd .. ----> To go one step back or go back to the previous directory
cd ----> To go back to the home
```

---

## 📍 Current Directory

```bash
pwd ----> Present working directory
```

---

## ❌ Deleting Files & Directories ⚠️

```bash
rm <file_name> ----> To Delete the file
rm f1
rm f2 f3 f5
```

```bash
rm -rf <directory_name> ----> To delete the directory
rm -rf sagar
rm -rf test test1
```

```bash
rm * ----> To delete all the files in the pwd
rm -rf * ---> To delete all the files and directories in the pwd 
rm *.c ----> To delete all the files with the extension .c
rm *.txt ---> To delete all the file with the extension .txt
```

> ⚠️ **Warning:** `rm -rf *` is dangerous — deletes everything permanently!

---

## ✍️ VI Text Editor

```bash
vi text editor
```

```bash
vi <File_name> -----> To create the file and edit the file
```

### 🔑 Modes

```bash
i -----> Insert mode
```

---

## 💾 Save & Exit

```bash
esc + :wq! ----> Save and Quit the file
esc + :w   ----> Save
esc + :q!  ----> Quit without saving
```

---

## 📖 File Viewing

```bash
cat <file_name> ----> To display the content of the file
```

---

## 🛠️ VI Editor Shortcuts

```bash
esc u -----> undo 
esc + :set nu ----> To set the line numbers in a file
esc + :set nonu ----> To remove the line numbers in a file
esc + :4   -----> It moves the cursor to the 4th line
```

---

## 🔍 Find and Replace in VI Editor

```bash
esc + :%s/<old_word>/<new_word>/ig    ------------> To find and replace the string
esc + :%s/linux/windows/ig
```

### 🧠 Breakdown

```
% -----> All the lines
s -----> substitute
g -----> Globally
i -----> case sensitve
```

---

### 🔁 Replace Variations

```bash
esc + :%s/<old_word>/<new_word>/ig  -----> To replace the string in all the lines
esc + :2s/<old_word>/<new_word>/ig  -----> replace the string in the 2nd line
esc + :2,3s/<old_word>/<new_word>/ig  ----> replace the string in 2nd to 3rd line
esc + :2,$s/<old_word>/<new_word>/ig  ----> replace the string from 2nd line to the end of the file
esc + :2s/<old_word>/<new_word>/ig | 5s/<old_word>/<new_word>/ig  ----> replace the string in 2nd and 5th line 
```

---

## ✂️ Delete Line in VI

```bash
esc + dd  ----> To delete the whole line in a file
```

---

## 🖨️ Print in Linux

```bash
echo ----> To print in linux
```

### 📌 Examples

```bash
echo "welcome to ss training"
```

**Output:**

```
welcome to ss training
```

```bash
echo -e "welcome \nss training"
```

**Output:**

```
welcome
ss training
```

---

## 📝 Assignment

👉 Display the contents of the file in reverse order

---

## 🎯 Visual Learning Flow

```
📁 Create → 📂 Navigate → 👀 View → ✍️ Edit → ❌ Delete

touch → cd → ls → vi → rm
```

---

## 🚀 Bonus Tip for Students

💡 Most used commands in real-time:

* `ls -lrt`
* `cd`
* `vi`
* `cat`
* `rm -rf` (⚠️ use carefully)

---

```

---

If you want next upgrade 🚀  
I can convert this into:
- :contentReference[oaicite:0]{index=0}
- :contentReference[oaicite:1]{index=1}
- :contentReference[oaicite:2]{index=2}

Just tell 👍 “PPT” or “PDF” or “Script”
```
