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