# 🐧 Linux Master Notes (Student Edition)

> 🚀 Clean • Visual • Beginner Friendly • GitHub Ready

---

## ✨ 1. File & Directory Basics

### 📁 Create Files

```bash
touch <file_name>
touch f1
touch f2 f3 f4
```

### 🧹 Clear Screen

```bash
clear
```

---

## 📂 Listing Files

```bash
ls
ls -l
ls -lt
ls -lrt
ls -lrth
```

💡 Tip:

* `-h` → Human readable size
* `-t` → Sort by time

---

## 📁 Directory Operations

```bash
mkdir <dir>
mkdir test test1 test2

cd <dir>
cd ..
cd ~
```

---

## 📍 Current Directory

```bash
pwd
```

---

## ❌ Delete Files

```bash
rm file
rm f1 f2
rm *.txt
rm -rf dir
rm -rf *
```

⚠️ **Danger:** `rm -rf *` deletes EVERYTHING in current directory

---

## ✍️ VI Editor Basics

```bash
vi file
```

| Mode | Action      |
| ---- | ----------- |
| i    | Insert      |
| esc  | Exit mode   |
| :wq! | Save & quit |
| :q!  | Quit        |

### 🔄 Find & Replace

```bash
:%s/old/new/ig
```

---

## 🖨️ Print Output

```bash
echo "Hello"
echo -e "Hello\nWorld"
```

---

## 🔁 Reverse File Content (Assignment)

```bash
tac file
```

---

# 🔥 2. Redirection & File Handling

### ➡️ Write

```bash
echo "hello" > file
```

### ➕ Append

```bash
echo "world" >> file
```

---

## 📋 Copy & Move

```bash
cp file1 file2
cp file dir/
cp -R dir1 dir2

mv file dir/
mv old new
```

---

## 🔢 Word Count

```bash
wc file
wc -l file
wc -w file
wc -c file
```

---

## 🔍 GREP (Search)

```bash
grep word file
grep -i word file
grep -v word file
grep -c word file
```

---

# 🔐 3. Permissions

```
rwx = 7
rw- = 6
r-- = 4
```

```bash
chmod 777 file
chmod 644 file
chmod u+rwx file
chmod o-r file
```

---

# 👤 Users & Groups

```bash
useradd user
passwd user
userdel user

su - user
```

### 🔑 Give Sudo Access

```bash
vi /etc/sudoers
user ALL=(ALL) NOPASSWD: ALL
```

---

# 🧠 System Info

```bash
who
whoami
uname -a
free -h
df -h
nproc
```

---

# 📊 4. File Viewing

```bash
head file
tail file
```

### 🎯 Example

```bash
head -8 file | tail -2
```

---

# 🔧 5. sed (Stream Editor)

```bash
sed 's/old/new/g' file
sed -i '2d' file
sed -n '5p' file
```

---

# ✂️ 6. cut & awk

### cut

```bash
cut -d " " -f1 file
```

### awk

```bash
awk '{print $1}' file
awk 'NR==2' file
```

---

# 🌳 7. Find & Tree

```bash
find -type f -name file
find -type f -empty
find -mtime -5
```

---

# 🔗 8. Links

```bash
ln -s file softlink
ln file hardlink
```

---

# 🌐 9. Networking

| Service | Port |
| ------- | ---- |
| SSH     | 22   |
| HTTP    | 80   |
| HTTPS   | 443  |

```bash
ping google.com
```

---

# 🔐 SSH

```bash
ssh user@ip
scp file user@ip:/path
rsync -avz file user@ip:/path
```

---

# ⚙️ 10. Processes & Services

```bash
ps -ef
top
kill -9 PID
```

### Services

```bash
systemctl start docker
systemctl stop docker
systemctl enable docker
```

---

# ⏱️ System Monitoring

```bash
uptime
date
```

---

# 🔥 Advanced Commands

### sort + uniq

```bash
sort file | uniq
```

### tee

```bash
ls -l | tee file
```

---

# 🌐 Ports & Networking

```bash
netstat -tulnp
```

---

# 🧵 Background Jobs

```bash
command &
jobs
fg %1
```

---

# 🕒 Timezone

```bash
timedatectl set-timezone Asia/Kolkata
```

---

# 🚀 BONUS (Added for Students)

## 📦 Package Managers

```bash
yum install nginx
apt install nginx
```

---

## 📁 Disk Usage Deep Dive

```bash
du -sh *
```

---

## 🔥 Find Non-Empty Files

```bash
find . -type f ! -empty
```

---

## 📦 Find Files >1MB

```bash
find . -type f -size +1M
```

---

## ❌ Delete Empty Files

```bash
find . -type f -empty | xargs rm
```

---

## 🧠 Sticky Bit (IMPORTANT)

```bash
chmod +t dir
```

👉 Only owner can delete files inside directory

Example: `/tmp`

---

## 📜 Login History

```bash
last
lastlog
```

---

## 🔐 Password Expiry

```bash
chage -M 30 user
```

---

## 🔄 Change Password

```bash
passwd user
```

---

# 🎯 Pro Tips

* Always use `-h` for readable output
* Avoid `rm -rf *` in production ⚠️
* Use `history` to track commands
* Use `alias` for shortcuts

---

# 🎉 Done!

> ⭐ Save this file in GitHub
> ⭐ Use it for revision
> ⭐ Teach like a pro!

---

## 🔥 Want Next Upgrade?

* Add diagrams (Kubernetes style)
* Add real-time labs
* Convert to PPT
* Add DevOps interview Q&A

Just tell me 👍
