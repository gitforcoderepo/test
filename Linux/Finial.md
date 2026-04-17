---

# 🐧 Linux Mastery Notes (Class 01 – Class 06)

<p align="center">
  <b>🚀 Complete Linux Training Notes — Beginner to Advanced</b><br>
  <i>Hands-on | DevOps | Real-Time Commands</i>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Linux-Training-blue?style=for-the-badge&logo=linux">
  <img src="https://img.shields.io/badge/Classes-01_to_06-green?style=for-the-badge">
  <img src="https://img.shields.io/badge/Focus-CLI_|_Admin_|_DevOps-orange?style=for-the-badge">
</p>

---

# 📅 Class -01 (30-03-2026)

---

## 📁 File Creation

```bash
touch <file_name> -----> To create the file_name
touch f1
touch f2 f3 f4

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

cd <directory_name> ----> To get into the directory
cd sagar

cd .. ----> To go one step back or go back to the previous directory
cd ----> To go back to the home
```

---

## 📍 Current Directory

```bash
pwd ----> Present working directory
```

---

## ❌ Deleting Files & Directories

```bash
rm <file_name> ----> To Delete the file
rm f1
rm f2 f3 f5

rm -rf <directory_name> ----> To delete the directory
rm -rf sagar
rm -rf test test1
```

---

### ⚠️ Danger Zone

```bash
rm * ----> To delete all the files in the pwd
rm -rf * ---> To delete all the files and directories in the pwd 
rm *.c ----> To delete all the files with the extension .c
rm *.txt ---> To delete all the file with the extension .txt
```

---

## ✍️ VI Text Editor

```bash
vi text editor

vi <File_name> -----> To create the file and edit the file

i -----> Insert mode

esc + :wq! ----> Save and Quit the file
esc + :w   ----> Save
esc + :q!  ----> Quit without saving
```

---

## 📄 File Content

```bash
cat <file_name> ----> To display the content of the file
```

---

## ⚙️ VI Extra Commands

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

```text
% -----> All the lines
s -----> substitute
g -----> Globally
i -----> case sensitve
```

```bash
esc + :%s/<old_word>/<new_word>/ig  -----> To replace the string in all the lines
esc + :2s/<old_word>/<new_word>/ig  -----> replace the string in the 2nd line
esc + :2,3s/<old_word>/<new_word>/ig  ----> replace the string in 2nd to 3rd line
esc + :2,$s/<old_word>/<new_word>/ig  ----> replace the string from 2nd line to the end of the file
esc + :2s/<old_word>/<new_word>/ig | 5s/<old_word>/<new_word>/ig  ----> replace the string in 2nd and 5th line 

esc + dd  ----> To delete the whole line in a file
```

---

## 🖨️ Print in Linux

```bash
echo ----> To print in linux

echo "welcome to ss training"
```

```text
output:
welcome to ss training
```

```bash
echo -e "welcome \nss training"
```

```text
output:
welcome
ss training
```

---

## 📝 Assignment

```text
Display the contents of the file in reverse order
```

---

# 📅 Class -02 (31-03-2026)

---

## 🔁 Redirect & Append

```bash
redirect (>) ----> used to write the output of a command to a file and if the file not present, it will create the new file
(replace the original content of the file)

echo "welcome" > <file_name>
echo "welcome" > test
```

```bash
append (>>) ----> it will write the output of a command at the end of the file and if the file not present, it will create the new file

echo "ss training" >> <file_name>
echo "ss training" >> test
```

```text
output:
welcome
ss training
```

---

## 📄 COPY

```bash
cp <file_1> <file_2> ----> Copy the content from file_1 to file_2 (act as redirect)
ex: test test1

cp <file> <directory> ----> To copy the file onto the directory
ex: cp test /home/ec2-user/demo1/test/

cp -R <dir_1> <dir_2> -----> To copy the data from dir_1 to dir_2
cp -R test2 demo1
```

---

## 🚚 Move

```bash
mv <file_1> <file_2>  ----> Move the file from file_1 to file_2
mv <file> <directory> ----> Move the file to the directory
mv <dir_1> <dir_2> ---> To move the directories from dir_1 to dir_2
```

---

## 📊 Word Count

```bash
wc <file_name> ----> To check the number of lines, words and characters in a file
wc -l <file_name> ---> prints only the number of lines in a file
wc -c <file_name> ---> Prints only the number of characters in a file
wc -w <file_name> ---> Prints only the number of words in a file

ex:
wc test
2  6 33 test
```

---

## 🔍 grep

```bash
grep -----> It is used to Search for a particular pattern/string in a file

grep <pattern> <file_name>
grep -w <pattern> <file_name>
grep -e <patten1> -e <pattern2> <file_name>
grep <^pattern> <file_name>
grep <pattern$> <file_name>
grep -v <pattern> <file_name>
grep -c <pattern> <file_name>
grep -i <pattern> <file_name>
```

---

# 📅 Class -03 (01-04-2026)

---

## 🔐 Permissions

```text
owner group others
rw-   r--   r--.
6     4     4
```

```text
r ---> read  ------> 2^2 ---> 4
w ---> write  -----> 2^1 ---> 2
x ---> execute ----> 2^0 ---> 1
```

```bash
chmod <permission> <file_name>
chmod -R <permission> <directory_name>

chmod 777 <file_name>
chmod 644 <file_name>
chmod 555 <file_name>
chmod 700 <file_name>
```

---

## 🔧 Symbolic Permissions

```bash
u ---> owner
g ---> group
o ---> others

chmod u+rwx <file_name>
chmod g+rw  <file_name>
chmod o-r <file_name>
chmod u-x <file_name>
```

---

## 👤 Users

```bash
sudo useradd <user_name>
sudo passwd <user_name>
sudo userdel <user_name>

getent passwd
cat /etc/passswd
```

---

## 🔄 Switch User

```bash
su - <user_name>
```

---

## 🛡️ Sudoers

```bash
vi /etc/sudoers

<user_name> ALL=(ALL) NOPASSWD: ALL
```

---

## 👥 Groups

```bash
sudo groupadd <group_name>
sudo groupdel <group_name>

getent group
cat /etc/group

sudo usermod -aG <group_name> <user_name>
```

---

## 🧾 Ownership

```bash
chown <user_name> <file>
chgrp <group_name> <file>

chown -R <user>:<group> <file>
```

---

## 🧠 Linux Architecture

```text
hardware ----> Kernal -----> Shell -----> Application ----> User
```

---

# 📅 Class -04 (02-04-2026)

---

## 📄 head / tail

```bash
head -5 <file>
tail -5 <file>
```

---

## 🔗 Pipe

```bash
command1 | command2
```

---

## ✏️ sed

```bash
sed 's/<old>/<new>/ig' <file>
sed -i '2d' <file>
```

---

## ✂️ cut

```bash
cut -d " " -f1 <file>
```

---

## 🧠 awk

```bash
awk '{print $1}' <file>
awk 'NR==2' <file>
```

---

## 🌳 tree

```bash
tree
```

---

## 🔍 find

```bash
find -type f -name <file>
find -mtime -5
find -empty
```

---

# 📅 Class -05 (03-04-2026)

---

## 🔗 Links

```bash
ln <file> hardlink
ln -s <file> softlink
```

---

## 🔐 SSH

```bash
ssh user@host
ssh -i key.pem user@host
```

---

## 📂 SCP

```bash
scp file user@host:/path
```

---

## ⚡ rsync

```bash
rsync -avz dir user@host:/path
```

---

## 🌐 Ports

```text
SSH 22
HTTP 80
HTTPS 443
FTP 21
```

---

# 📅 Class -06 (04-04-2026)

---

## ⚙️ Process

```bash
ps -ef
top
kill -9 <PID>
```

---

## 🔧 Services

```bash
systemctl start docker
systemctl stop docker
systemctl enable docker
```

---

## 📊 System Info

```bash
free -h
df -h
nproc
uptime
```

---

## 🌐 Networking

```bash
netstat -tulnp
ping google.com
```

---

## 🧠 Advanced

```bash
history
alias ll="ls -l"
export VAR="value"
```

---

## 🔁 Background Jobs

```bash
command &
jobs
fg %1
```

---

## 🕒 Time

```bash
timedatectl
date
```

---

# 🧪 Assignments

```text
1. Command to list the volume block 
2. What is stickybit
3. Create user with sudo permission
4. Check last login user
5. Extend password expiry
6. Install Tomcat
7. Find large files
8. Delete empty files
9. Learn telnet, screen
10. Zombie process
11. Block IP
```

---

# 💡 Final Note

> **Nothing removed. Only enhanced.** ✅
> Your original teaching flow is preserved 100%.

---
Just say: **“make DevOps trainer pack”** 😎
