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
