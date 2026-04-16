
# SSH Logs Analysis with Splunk

## 📌 Project Overview
This project demonstrates how Splunk can be used to monitor and analyze SSH activity.  
The dashboard provides visibility into login attempts, authentication patterns, and potential brute force attacks.

---

## 🗂️ Project Setup Steps

### 1. Prepare the Environment
- Install **Splunk Enterprise** (tested on version 10.2.2).
- Ensure you have access to the Splunk web interface (`http://localhost:8000` by default).
- Download and install **Ubuntu** (optional, if you want to generate fresh SSH logs).

### 2. Collect SSH Logs
- Extract the provided **zip file** containing SSH logs.
- Place the extracted log files into a folder, e.g., `sample_logs/`.
- Verify logs contain authentication events (`/var/log/auth.log` or equivalent).

### 3. Ingest Logs into Splunk
- Navigate to **Settings → Add Data → Upload Files**.
- Upload the extracted SSH log files.
- Assign a source type (e.g.,`ssh_logs`).
- Save and index the data.

### 4. Create SPL Queries
Use Splunk Processing Language (SPL) to analyze:
```spl
-index=ssh_logs | stats count as "total ssh events" 
-index=ssh_logs | stats count as "successful ssh events" 
-index=ssh_logs | stats count as "failed ssh events" 



## 🔐 SSH Log Monitoring Dashboard

<img width="1871" height="1053" alt="Screenshot 2026-04-15 233731" src="https://github.com/user-attachments/assets/d4ecc073-4188-42c9-b424-082061e8ed4a" />
<img width="1876" height="948" alt="Screenshot 2026-04-15 233627" src="https://github.com/user-attachments/assets/a1abba85-6aa8-4918-bcf3-43283f547377" />
<img width="1897" height="1054" alt="Screenshot 2026-04-15 233530" src="https://github.com/user-attachments/assets/7e3b6a9a-6daa-43ec-ad04-75929492a62c" />
<img width="1891" height="982" alt="Screenshot 2026-04-13 115247" src="https://github.com/user-attachments/assets/14529ead-8131-45cc-b207-db7375b539c3" />
<img width="1913" height="1016" alt="Screenshot 2026-04-13 115234" src="https://github.com/user-attachments/assets/e94399ab-ca09-4f28-98cd-f46ea8bae8db" />

## 🔐 SSH Log Monitoring Dashboard

![Screenshot 2026-04-15 233731](https://github.com/user-attachments/assets/d4ecc073-4188-42c9-b424-082061e8ed4a)





