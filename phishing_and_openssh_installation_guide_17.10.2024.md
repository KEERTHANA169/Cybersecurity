**Phishing and OpenSSH Installation on Kali Linux**

This document outlines the steps for setting up a phishing tool (Zphisher) and installing OpenSSH on Kali Linux, including troubleshooting common issues during the installation process.

#### Steps:
1. **Update Package Lists:**
   ```bash
   sudo apt update
   ```

2. **Install OpenSSH Client and Server:**
   ```bash
   sudo apt install openssh-client openssh-server
   ```

3. **Start the SSH Service:**
   ```bash
   sudo systemctl start ssh
   ```

4. **Enable SSH Service to Start on Boot:**
   ```bash
   sudo systemctl enable ssh
   ```

5. **Edit APT Source List:**
   ```bash
   sudo nano /etc/apt/source.list
   ```

6. **Update Again:**
   ```bash
   sudo apt update
   ```
