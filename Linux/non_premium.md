Here’s your **GitHub-ready premium Markdown (.md)** version — cleaned, structured, and visually appealing with better formatting, spacing, and consistency 👇

---

# 🐧 Linux Basics - Class 01

### 📅 30-03-2026

💡 *Learn Linux the practical way — step by step*

---

## 📚 Table of Contents

* [📁 File Creation](#-file-creation)
* [📂 Listing Files & Directories](#-listing-files--directories)
* [📁 Directory Management](#-directory-management)
* [📍 Current Directory](#-current-directory)
* [❌ Deletion](#-deleting-files--directories)
* [✍️ VI Text Editor](#️-vi-text-editor)
* [🔍 Find & Replace](#-find-and-replace-in-vi-editor)
* [🖨️ Print](#️-print-in-linux)
* [🧪 Practice Lab](#-practice-lab)
* [📝 Assignment](#-assignment)

---

## 🧠 Learning Flow

```text
Create → Navigate → View → Edit → Delete
touch → cd → ls → vi → rm
```

---

## 📁 File Creation

```bash
# Create files
touch <file_name>
touch f1
touch f2 f3 f4

# Clear screen
clear
```

---

## 📂 Listing Files & Directories

```bash
ls        # List files & directories
ls -l     # Long format
ls -lt    # Sort by time (latest first)
ls -lrt   # Reverse order (oldest first)
ls -lrth  # Human-readable size + reverse order
```

---

## 📁 Directory Management

```bash
# Create directory
mkdir <directory_name>
mkdir sagar
mkdir test test1 test2

# Navigate
cd <directory_name>
cd sagar

# Go back
cd ..

# Go to home
cd
```

---

## 📍 Current Directory

```bash
pwd   # Present Working Directory
```

---

## ❌ Deleting Files & Directories

```bash
# Delete files
rm <file_name>
rm f1
rm f2 f3 f5

# Delete directories
rm -rf <directory_name>
rm -rf sagar
rm -rf test test1
```

⚠️ **Danger Zone**

```bash
rm *        # Delete all files
rm -rf *    # Delete everything (files + directories)

rm *.c      # Delete all .c files
rm *.txt    # Delete all .txt files
```

---

## ✍️ VI Text Editor

```bash
# Open or create file
vi <file_name>
```

### 🔹 Modes

* `i` → Insert mode
* `Esc` → Command mode

### 🔹 Save & Exit

```bash
Esc + :wq!   # Save & Quit
Esc + :w     # Save
Esc + :q!    # Quit without saving
```

### 🔹 Viewing File

```bash
cat <file_name>
```

### 🔹 Useful Commands

```bash
Esc + u          # Undo
Esc + :set nu    # Show line numbers
Esc + :set nonu  # Hide line numbers
Esc + :4         # Go to line 4
Esc + dd         # Delete entire line
```

---

## 🔍 Find and Replace in VI Editor

```bash
Esc + :%s/<old>/<new>/ig
```

### 🔹 Example

```bash
:%s/linux/windows/ig
```

### 🔹 Meaning

* `%` → All lines
* `s` → Substitute
* `g` → Global (all occurrences)
* `i` → Case insensitive

### 🔹 Advanced Usage

```bash
:%s/old/new/ig        # Entire file
:2s/old/new/ig        # Line 2 only
:2,3s/old/new/ig      # Line 2 to 3
:2,$s/old/new/ig      # Line 2 to end
:2s/old/new/ig | 5s/old/new/ig   # Line 2 & 5
```

---

## 🖨️ Print in Linux

```bash
echo "welcome to ss training"
```

### 🔹 Output

```text
welcome to ss training
```

### 🔹 Multi-line Print

```bash
echo -e "welcome \nss training"
```

```text
welcome
ss training
```

---

## 🧪 Practice Lab (🔥 Must Try)

```bash
# Create files
touch file1 file2 file3

# Create directory
mkdir demo

# Navigate
cd demo

# Create file inside
touch test.txt

# List files
ls -lrt

# Go back
cd ..

# Delete file
rm file1
```

---

## 📝 Assignment

🎯 **Task:** Display the contents of a file in reverse order

💡 *Hint: Use commands like `tac`*

---

## 💡 Pro Tips

* ⚡ Use `Tab` for auto-completion
* ⬆️ Use `↑` for previous commands
* 🚀 Practice daily for speed

---

## ⭐ Keep Learning

> **"Linux is not learned by reading — it is mastered by doing."**

---

If you want next level upgrade 😎 I can:

* 🔥 Add badges (GitHub style)
* 🎨 Add colors using shields.io
* 📊 Add diagrams (Mermaid)
* 🎥 Convert this into PPT slides directly

Just say: **“make it ultra premium”** 🚀
