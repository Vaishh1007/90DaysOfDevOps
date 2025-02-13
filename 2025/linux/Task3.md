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