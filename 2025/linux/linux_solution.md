# Week 2: Linux System Administration & Automation

Welcome to Week 2 of the **90 Days of DevOps - 2025 Edition!** This week focuses on Linux system administration and automation, covering user management, file permissions, log analysis, process control, volume mounts, and shell scripting.

## 🚀 Project: DevOps Linux Server Monitoring & Automation
Imagine managing a Linux-based production server where users, logs, and processes must be efficiently handled. You will perform real-world tasks such as log analysis, volume management, and automation to enhance your DevOps skills.

---

## 📌 Tasks

### 1️⃣ User & Group Management
#### **Task:**
- Create a user `devops_user` and add them to a group `devops_team`.
- Set a password and grant sudo access.
- Restrict SSH login for certain users in `/etc/ssh/sshd_config`.

#### **Commands:**
```bash
# Create user and add to group
sudo groupadd devops_team
sudo useradd -m devops_team 
sudo gpasswd -M devops_user devops_team

# Set a password 
sudo passwd devops_user

# Grant sudo access
usermod -aG sudo devops_user

# Restrict SSH access
sudo nano /etc/ssh/sshd_config
# Add: DenyUsers restricted_user
sudo systemctl restart sshd
```

---

### 2️⃣ File & Directory Permissions
#### **Task:**
- Create `/devops_workspace` and a file `project_notes.txt`.
- Set permissions:
  - Owner: edit
  - Group: read-only
  - Others: no access

#### **Commands:**
```bash
mkdir /devops_workspace
touch /devops_workspace/project_notes.txt
chmod 240 /devops_workspace/project_notes.txt
ls -l /devops_workspace/project_notes.txt
```

---

### 3️⃣ Log File Analysis with AWK, Grep & Sed
#### **Task:**
- Download log file `Linux_2k.log`and their data will be stored in the file `app.log` 
- Extract insights:
  - Find occurrences of "error".
  - Extract timestamps and log levels.
  - Replace IPs with `[REDACTED]`.
  - Find most frequent log entries.

#### **Commands:**
```bash
wget https://github.com/yourrepo/LogHub/Linux_2k.log

# Find "error"
grep -i 'error' app.log

# Extract timestamps and log levels
awk '{print $1, $2}' app.log | head -10

# Mask IP addresses
sed -E 's/[0-9]+\.[0-9]+\.[0-9]+\.[0-9]+/[REDACTED]/g' app.log > sanitized_log.log

# Find most frequent log entry
awk '{print $0}' app.log | sort | uniq -c | sort -nr | head -10
```

---

### 4️⃣ Volume Management & Disk Usage
#### **Task:**
- Create `/mnt/devops_data`.
- Mount a new volume (or loop device for practice).
- Verify using `df -h` and `mount`.

#### **Commands:**
```bash
mkdir /mnt/devops_data

#create a volume of type General Purpose SSD(gp3) in your aws account and attched resources /dev/sdf
sudo mkfs.ext4 /dev/xvdf 
sudo mount /dev/xvdf /mnt/devops_data

df -h
mount | grep devops_data
```

---

### 5️⃣ Process Management & Monitoring
#### **Task:**
- Start a background process.
- Use `ps`, `top`, and `htop` to monitor.
- Kill the process.

#### **Commands:**
```bash
ping google.com > ping_test.log &
ps aux | grep ping
top
htop
pkill ping 
kill <PID> 
```

---

### 6️⃣ Automate Backups with Shell Scripting
#### **Task:**
- Write a script to back up `/devops_workspace`.
- Save as `backup_$(date +%F).tar.gz` in `/backups`.
- Schedule with `cron`.
- Display success message in **green text**.



## ✅ Conclusion
By completing these tasks, you have gained hands-on experience in:
- **User & group management**
- **File permissions & access control**
- **Log file analysis with Linux commands**
- **Volume management & disk usage monitoring**
- **Process control & monitoring**
- **Shell scripting & automation**

This week builds foundational DevOps skills, preparing you for automation, CI/CD, and infrastructure as code. Keep going strong! 🚀

