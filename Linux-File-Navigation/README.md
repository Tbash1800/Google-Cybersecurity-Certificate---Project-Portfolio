# Linux File Navigation and Analysis

## Project Overview
As a Security Analyst, navigating the Linux file system and analyzing system logs and user data is a daily responsibility. This project demonstrates foundational skills in using the Linux command line (Bash) to locate specific files, inspect directory structures, audit user management records, and review security logs for potential issues.

* **Objective:** Locate and analyze specific files within the `/home/analyst` directory structure to audit new user additions and inspect server log trends.
* **Skills Learned:** Linux Command Line Interface (CLI), File System Navigation, Directory Auditing, Log Inspection.
* **Tools Used:** Bash Shell, Linux Core Utilities (`pwd`, `ls`, `cd`, `cat`, `head`).

---

## Lab Scenario
The objective of this lab is to locate and analyze specific files within the `/home/analyst` directory. The task requires:
1. Verifying the current working directory and listing its contents.
2. Navigating to the `reports` directory to locate user audit data.
3. Inspecting the contents of `Q1_added_users.txt`.
4. Navigating to the `logs` directory and viewing the first 10 entries of the server log file.

---

## Step-by-Step Execution

### Step 1: Check Current Directory and List Contents
First, verify the current working directory to establish a baseline. Then, list the contents to find the target directories.

```bash
pwd
ls
```

**Output:**
```text
/home/analyst
logs  projects  reports  temp
```
*Insight: The root of the analyst home directory contains four primary folders: logs, projects, reports, and temp.*

### Step 2: Navigate to Reports and Identify User Data
Change directories into `reports` to locate the user subdirectories.

```bash
cd reports
ls
```

**Output:**
```text
users
```

### Step 3: Inspect Q1 Added Users
Navigate deeper into the `users` subdirectory and display the full contents of `Q1_added_users.txt` to review newly onboarded employees.

```bash
cd users
ls
cat Q1_added_users.txt
```

**Output:**
```text
employee_id  username  department
1001         bmoreno   Marketing
1026         apatel    Human Resources
1041         cgriffin  Sales
1104         mreed     Information Technology
1177         aezra     Human Resources
1188         noshiro   Finance
```
*Insight: This file tracks six new user accounts across various departments, including Marketing, HR, Sales, IT, and Finance. This data is critical for Identity and Access Management (IAM) reconciliation.*

### Step 4: Analyze Server Logs
Return to the home directory, navigate to the `logs` directory, and inspect the first 10 lines of `server_logs.txt` to check for early system errors or warnings.

```bash
cd ~
cd logs
ls
head server_logs.txt
```

**Output:**
```text
2022-09-28 13:55:55 info    User logged on successfully
2022-09-28 13:56:22 error   The password is incorrect
2022-09-28 13:56:48 warning The file storage is 75% full
2022-09-28 15:55:55 info    User logged on successfully
2022-09-28 15:56:22 error   The username is incorrect
2022-09-28 15:56:48 warning The file storage is 90% full
2022-09-28 16:55:55 info    User navigated to settings page
2022-09-28 16:56:22 error   The password is incorrect
2022-09-28 16:56:48 warning The current user’s password expires in 15 days
2022-09-29 13:55:55 info    User logged on successfully
```

---

## Key Takeaways and Security Insights
* **Log Auditing:** Using the `head` command allowed for a quick triage of the log file. The logs reveal multiple authentication failures (`error: The password is incorrect`) and storage warnings (`warning: The file storage is 90% full`), which require immediate administrative attention.
* **Command Efficiency:** Mastering basic navigation commands (`cd`, `ls`, `pwd`) and file viewers (`cat`, `head`) forms the operational foundation needed to perform fast, effective incident response and forensic collection in Linux-based environments.
<img width="685" height="767" alt="Screenshot 2026-07-17 at 4 23 23 AM" src="https://github.com/user-attachments/assets/650f8c20-d4f9-41e5-8019-6e6cb69ee572" />
