Yes 👍 — here’s your **Linux Notes converted into a clean PPT-style Markdown (slide format)**.
You can directly use this in **Marp / HackMD / VS Code Markdown PPT extensions**.

---

```markdown
<!-- _class: lead -->
# 🐧 LINUX FUNDAMENTALS
## DevOps Training Notes
### Om-Tech

---

# 📁 File Operations

## Create Files
```

touch f1
touch f2 f3 f4

```

## Clear Screen
```

clear

```

---

# 📂 Listing Files

```

ls
ls -l
ls -lt
ls -lrt
ls -lrth

```

---

# 📁 Directory Management

```

mkdir test
mkdir test1 test2

cd test
cd ..
cd

```

---

# 📍 Current Directory

```

pwd

```

---

# ❌ Delete Files

```

rm f1
rm -rf test
rm *
rm -rf *
rm *.txt

```

---

# ✍️ VI Editor

## Open File
```

vi file.txt

```

## Modes
- i → Insert  
- esc :wq → Save & Exit  
- esc :q! → Exit  

---

# 🔍 VI Shortcuts

- undo → `esc u`  
- line numbers → `:set nu`  
- go to line → `:4`  
- delete line → `dd`  

---

# 🔁 Find & Replace

```

:%s/linux/windows/ig

```

---

# 🖨 Echo Command

```

echo "welcome"
echo -e "hello\nworld"

```

---

# 🔁 Redirect & Append

```

echo "hello" > file
echo "world" >> file

```

---

# 📄 Copy & Move

```

cp file1 file2
cp file dir/

mv file1 file2
mv file dir/

```

---

# 🔢 Word Count

```

wc file
wc -l file
wc -w file
wc -c file

```

---

# 🔎 Grep

```

grep "text" file
grep -i "text" file
grep -v "text" file
grep -c "text" file

```

---

# 🔐 Permissions

## Numeric
```

chmod 777 file
chmod 644 file

```

## Symbolic
```

chmod u+rwx file
chmod g+rw file
chmod o-r file

```

---

# 🔐 UMASK

```

umask 002
umask 000

```

---

# 🔑 SUDO

```

sudo command
sudo su -
exit

```

---

# 👤 User Management

```

useradd user1
passwd user1
userdel user1

```

---

# 🔄 Switch User

```

su - user1

```

---

# 👥 Groups

```

groupadd dev
groupdel dev
usermod -aG dev user1

```

---

# 📦 Ownership

```

chown user file
chgrp group file
chown user:group file

```

---

# 🧠 Linux Architecture

```

Hardware → Kernel → Shell → Application → User

```

---

# 📊 System Commands

```

who
whoami
uname -a
free -h
df -h
nproc

```

---

# 📄 Head & Tail

```

head file
head -5 file

tail file
tail -5 file

```

---

# 🔗 Pipe

```

head -8 file | tail -2

```

---

# ✏️ SED

```

sed 's/old/new/ig' file
sed -i '2d' file

```

---

# ✂️ CUT

```

cut -d " " -f1 file

```

---

# 🧮 AWK

```

awk '{print $1}' file
awk 'NR==2' file

```

---

# 🌳 Tree

```

yum install tree
tree

```

---

# 🔍 FIND

```

find -type f -name file
find -mtime -5
find -type f -empty

```

---

# 🔗 Links

## Soft Link
```

ln -s file link

```

## Hard Link
```

ln file link

```

---

# 🌐 SSH / SCP / RSYNC

```

ssh user@host
scp file user@host:/path
rsync -avz file user@host:/path

```

---

# 📡 Network

```

ping google.com

```

---

# ⚙️ Process

```

ps -ef
top
kill -9 PID

```

---

# 🔧 Services

```

systemctl start docker
systemctl stop docker
systemctl enable docker

```

---

# 📜 History

```

history

```

---

# ⚡ Alias

```

alias ll="ls -l"

```

---

# 🌱 Environment Variable

```

export NAME="Linux"
echo $NAME

```

---

# 🔄 Sort & Uniq

```

sort file | uniq

```

---

# 📝 Tee

```

ls -l | tee file

```

---

# 🌐 Netstat

```

netstat -tulnp

```

---

# ⚡ Background Jobs

```

command &
jobs
fg %1

```

---

# 🕒 Date & Time

```

date
timedatectl

```

---

# 🎯 Assignments

- sticky bit  
- inode usage  
- zombie process  
- boot sequence  
- iptables  
- screen command  

---

<!-- _class: lead -->
# 🙌 THANK YOU
## Happy Learning 🚀
```

---

If you want next level 🔥
I can also:

* Convert this into **actual .pptx file**
* Add **icons + colors + diagrams**
* Make **DevOps-ready presentation (YouTube style)**
