# Linux Server Hardening  

## Objective  
The goal of this task was to secure a Linux Ubuntu server by applying system hardening techniques. The focus areas included:  
- Configuring and enforcing firewall rules  
- Hardening SSH access  
- Enabling brute-force attack protection with Fail2ban  

---

## System Overview (Before Hardening)  
The server was initially in a default state with minimal security configurations:  
- Multiple open ports  
- Default SSH settings (root login and password authentication enabled)  
- No brute-force protection in place  

📂 Screenshots are stored in `before_screenshots/`:  
- `ports_before.png` – List of open ports  
- `ufw_before.png` – Firewall status (inactive)  
- `ssh_config_before.png` – Default SSH configuration  
- `fail2ban_before.png` – Fail2ban not installed/running  

---

## Hardening Steps  

### 1. Firewall (UFW)  
- Installed and configured **UFW (Uncomplicated Firewall)**  
- Rules applied:  
  - Block all incoming connections  
  - Allow all outgoing connections  
  - Allow **SSH only** (port 22)  

### 2. SSH Hardening  
- Edited `/etc/ssh/sshd_config` to improve security:  
  - Disabled **root login**  
  - Disabled **password authentication** (enforcing key-based login)  
  - Allowed only the user **student** to log in  

### 3. Fail2ban  
- Installed and enabled **Fail2ban**  
- Configured to monitor SSH login attempts  
- Protects against brute-force attacks  

### 4. Verification  
- Confirmed only essential ports are open  
- Validated firewall rules are active  
- Ensured SSH login is secure  
- Verified Fail2ban is running  

---

## System State (After Hardening)  
The server is now in a hardened state:  
- Only **SSH port** open and secured  
- Firewall properly configured  
- Fail2ban actively protecting the system  

📂 Screenshots are stored in `after_screenshots/`:  
- `ports_after.png` – List of open ports after hardening  
- `ufw_after.png` – Firewall rules applied  
- `ssh_config_after.png` – Hardened SSH configuration  
- `fail2ban_after.png` – Fail2ban service running  

---

## Commands Used  
A complete list of commands executed during this task is available in **[commands.txt](./commands.txt)**.  

---

## Notes  
- **tcpdump/PCAP capture** was skipped due to VirtualBox networking limitations.  
- All other hardening steps were fully implemented and verified.  
