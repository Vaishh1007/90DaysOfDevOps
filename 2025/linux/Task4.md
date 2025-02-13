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
