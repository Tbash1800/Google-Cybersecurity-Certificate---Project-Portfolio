# Lab: Managing Software with APT in Linux

## 🎯 Objective
To practice package management in a Linux environment by using the Advanced Package Tool (APT) to install, verify, uninstall, and list security applications like Suricata and tcpdump.

## 🛠️ Tools & Commands Summary

| Step | Action | Linux Command | Expected Outcome / Verification |
| :---: | :--- | :--- | :--- |
| **1** | Confirm APT Installation | `apt --version` | Displays the current version of the APT package manager. |
| **2** | Install Suricata | `sudo apt update && sudo apt install -y suricata` | System updates indexes and installs the Suricata IDS application. |
| **3** | Verify Suricata | `suricata --version` | Confirms successful installation by outputting the Suricata version. |
| **4** | Uninstall Suricata | `sudo apt remove -y suricata` | Uninstalls Suricata to practice software removal and cleanup. |
| **5** | Verify Removal | `suricata --version` | Confirms removal; terminal will state the command is not found. |
| **6** | Install tcpdump | `sudo apt install -y tcpdump` | Installs the tcpdump network packet analyzer tool. |
| **7** | List Applications | `apt list --installed` | Generates a complete database list of all active tools on the system. |
| **8** | Reinstall Suricata | `sudo apt install -y suricata` | Reinstalls Suricata so both security tools coexist on the environment. |
| **9** | Final Verification | `tcpdump --version` <br> `suricata --version` | Validates that both network security tools are fully active. |

---

## 📝 Detailed Step-by-Step Breakdown

### Section 1: Verifying the Package Manager
Before managing software, it is vital to ensure the core package manager is operational.
```bash
apt --version
```

### Section 2: Suricata Lifecycle (Installation & Removal)
I installed the Suricata intrusion detection tool, verified its path, and then removed it to demonstrate system cleanup.
```bash
# Install
sudo apt update && sudo apt install -y suricata
suricata --version

# Remove
sudo apt remove -y suricata
suricata --version
```

### Section 3: Concurrent Tool Management
I deployed tcpdump alongside a fresh installation of Suricata to verify that multiple security utilities can be managed and audited simultaneously.
```bash
# Install tcpdump and audit system
sudo apt install -y tcpdump
apt list --installed

# Reinstall Suricata for dual-tool verification
sudo apt install -y suricata
```

---

## 📸 Lab Evidence
* **APT Verification:** `<img width="690" height="770" alt="The APT Version" src="https://github.com/user-attachments/assets/704b234e-28a3-44ad-867c-d9f2c1aba687" />
* **The Intermediate Audit :<img width="689" height="771" alt="The Int" src="https://github.com/user-attachments/assets/ee07567a-9a2a-4d62-9122-9feffe176a9f" />

* **Final Status:**: <img width="687" height="772" alt="End of lab" src="https://github.com/user-attachments/assets/a525ba33-3226-4c95-8d14-7a04d8cf2436" />
