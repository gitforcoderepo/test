# 🐧 Linux Complete Notes (Beautified – Full Content Preserved)

> 🚀 **All original content preserved** • Enhanced formatting • Student-friendly visuals

---

# 📘 Linux

---

## ✨ Class -01

---

## 📁 File Creation

```bash
touch <file_name> -----> To create the file_name
touch f1
touch f2 f3 f4
```

## 🧹 Clear Screen

```bash
clear ----> To clean the screen
```

---

## 📂 List Files & Directories

```bash
ls -----> List all the files and directories
ls -l ---> List all the files and directories in the long format
ls -lt ---> List the files and directories based on the time
ls -lrt --> List the files in the reverse order
ls -lrth --> list the files in the reverse order with the size
```

---

## 📁 Directory Operations

```bash
mkdir <directory_name> -----> To create the directory
mkdir sagar
mkdir test test1 test2

cd <directory_name> ----> To get into the directory
cd sagar

cd .. ----> To go one step back
cd ----> To go back to home
```

---

## 📍 Present Working Directory

```bash
pwd ----> Present working directory
```

---

## ❌ Delete Files & Directories

```bash
rm <file_name>
rm f1
rm f2 f3 f5

rm -rf <directory_name>
rm -rf sagar
rm -rf test test1

rm * ----> delete all files
rm -rf * ---> delete all files and directories ⚠️
rm *.c
rm *.txt
```

---

## ✍️ VI Editor

```bash
vi <file_name>
```

### Modes

* `i` → Insert mode
* `esc` → Exit mode

### Save & Quit

```bash
esc + :wq! ----> Save and Quit
esc + :w ----> Save
esc + :q! ----> Quit without saving
```

### Other Commands

```bash
cat <file_name>
esc u ----> undo
esc + :set nu ----> show line numbers
esc + :set nonu ----> hide line numbers
esc + :4 ----> move to 4th line
```

---

## 🔄 Find & Replace (VI)

```bash
:%s/<old>/<new>/ig
```

### Variations

```bash
:2s/<old>/<new>/ig
:2,3s/<old>/<new>/ig
:2,$s/<old>/<new>/ig
:2s/... | 5s/...
```

---

## 🖨️ Print

```bash
echo "welcome to ss training"

echo -e "welcome \nss training"
```

---

## 🎯 Assignment

* Display file in reverse order

---

# ✨ Class -02

---

## 🔁 Redirection

```bash
> ----> overwrite
>> ----> append

echo "welcome" > test
echo "ss training" >> test
```

---

## 📋 Copy

```bash
cp <file1> <file2>
cp file dir/
cp -R dir1 dir2
```

---

## 🚚 Move

```bash
mv file1 file2
mv file dir/
mv dir1 dir2
```

---

## 🔢 Word Count

```bash
wc file
wc -l file
wc -c file
wc -w file
```

---

## 🔍 GREP

```bash
grep pattern file
grep -w pattern file
grep -e p1 -e p2 file
grep ^pattern file
grep pattern$ file
grep -v pattern file
grep -c pattern file
grep -i pattern file
```

---

# 🔐 Permissions

```
r = 4
w = 2
x = 1
```

```bash
chmod 777 file
chmod 644 file
chmod 555 file
chmod 700 file
```

### Symbolic

```bash
chmod u+rwx file
chmod g+rw file
chmod o-r file
chmod u-x file
```

---

# ✨ Class -03

---

## 🧠 umask

```
file = 666
dir = 777
```

```bash
umask 002
```

---

## 🔑 sudo

```bash
sudo command
sudo su -
exit
```

---

## 👤 Users

```bash
useradd user
passwd user
userdel user
```

```bash
su - user
```

---

## 👥 Groups

```bash
groupadd group
groupdel group
usermod -aG group user
```

---

## 🧾 Ownership

```bash
chown user file
chgrp group file
chown user:group file
```

---

## 🧠 Linux Architecture

```
Hardware → Kernel → Shell → Application → User
```

---

## 📊 System Commands

```bash
who
whoami
hostname
uname -a
free -h
df -h
nproc
```

---

# ✨ Class -04

---

## 📄 File Viewing

```bash
head file
tail file
```

---

## 🔗 Pipe

```bash
head -8 file | tail -2
```

---

## 🔧 sed

```bash
sed 's/old/new/g' file
sed -i '2d' file
sed -n '5p' file
```

---

## ✂️ cut

```bash
cut -d " " -f1 file
```

---

## ⚡ awk

```bash
awk '{print $1}' file
awk 'NR==2' file
```

---

## 🌳 find

```bash
find -type f -name file
find -type f -empty
find -mtime -5
```

---

# ✨ Class -05

---

## 🔗 Links

```bash
ln -s file softlink
ln file hardlink
```

---

## 🌐 Networking

| Service | Port |
| ------- | ---- |
| SSH     | 22   |
| HTTP    | 80   |
| HTTPS   | 443  |

```bash
ping google.com
```

---

## 🔐 SSH / SCP / RSYNC

```bash
ssh user@ip
scp file user@ip:/path
rsync -avz file user@ip:/path
```

---

# ✨ Class -06

---

## ⚙️ Processes

```bash
ps -ef
top
kill -9 PID
```

---

## 🔄 Services

```bash
systemctl start docker
systemctl stop docker
systemctl enable docker
```

---

## ⏱️ Monitoring

```bash
uptime
date
```

---

## 🔥 Advanced

```bash
sort file | uniq
ls -l | tee file
netstat -tulnp
```

---

## 🧵 Background Jobs

```bash
command &
jobs
fg %1
```

---

## 🕒 Timezone

```bash
timedatectl set-timezone Asia/Kolkata
```

---

# 🎯 Assignments

* Volume block command
* Sticky bit
* Create sudo user
* Login history
* Password expiry
* Change password
* telnet
* bashrc vs bash_profile
* screen command
* rollback
* inode usage
* booting sequence
* zombie process
* block IP
* iptables

---

# 🎉 Notes Ready!

> 💡 100% original content preserved
> 🎨 Beautified for GitHub + Students
> 🚀 Ready to teach & upload

---

## 🔥 Next Upgrade?

* Add diagrams
* Convert to PPT
* Add labs

👉 Just tell me 👍

---

# 🎬 Visual Learning (GIF Demos)

> 📌 These GIFs help students quickly understand command behavior (add these to your repo `/assets` folder)

### 📂 ls Command Demo

![ls demo](assets/ls-demo.gif)

### 📁 Navigation Demo (cd, pwd)

![cd demo](assets/cd-demo.gif)

### ❌ rm Command Demo

![rm demo](assets/rm-demo.gif)

### ✍️ vi Editor Demo

![vi demo](assets/vi-demo.gif)

### 🔍 grep Demo

![grep demo](assets/grep-demo.gif)

---

# 🧠 Real-World Scenarios (Very Important for Students)

## 📂 File Handling

👉 *Scenario:* Developer creates log files and needs to clean old ones

```bash
rm *.log
```

---

## 🔍 grep

👉 *Scenario:* Searching error logs in production

```bash
grep ERROR app.log
```

---

## 🔐 Permissions

👉 *Scenario:* Restricting access to sensitive config files

```bash
chmod 600 secrets.txt
```

---

## 👤 Users

👉 *Scenario:* Creating new developer account with sudo access

```bash
useradd dev1
passwd dev1
```

---

## 🌐 SSH

👉 *Scenario:* Connecting to AWS EC2 server

```bash
ssh ec2-user@<ip>
```

---

## ⚙️ Processes

👉 *Scenario:* Killing stuck application

```bash
kill -9 PID
```

---

## 🔄 Services

👉 *Scenario:* Restarting nginx after config change

```bash
systemctl restart nginx
```

---

# 📊 Linux Architecture Diagram

```
+----------------------+
|        User          |
+----------+-----------+
           |
+----------v-----------+
|     Applications     |
+----------+-----------+
           |
+----------v-----------+
|        Shell         |
+----------+-----------+
           |
+----------v-----------+
|        Kernel        |
+----------+-----------+
           |
+----------v-----------+
|   Hardware (CPU,RAM) |
+----------------------+
```

---

## 🧠 How It Works (Simple Flow)

```
User → Command → Shell → Kernel → Hardware → Output
```

---

# 🚀 Pro Teaching Add-ons

## 🎯 Mini Lab Idea

```bash
# Create project
mkdir devops && cd devops

# Create files
touch app.log error.log

# Add content
echo "ERROR: failed" >> error.log

# Search error
grep ERROR error.log
```

---

## 💡 Interview Booster

* Difference between softlink & hardlink
* chmod 777 vs 755
* grep vs awk vs sed
* top vs ps

---

# 🎉 Ultimate Notes Ready

> 🔥 Now this is **YouTube + Classroom Ready**
> 🎬 Visual + Practical + Real-world learning

---
