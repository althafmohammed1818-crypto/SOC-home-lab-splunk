
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

![Screenshot 2026-04-13 115234.png]https://github.com/althafmohammed1818-crypto/SOC-home-lab-splunk/blob/b5e5667dc8f62b842d6d3ab4eab9583c47a6bc30/Screenshot%202026-04-13%20115234.png





