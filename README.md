# Linux Server Hardening – Internship Task 4

## Objective
Secure a Linux Ubuntu server by applying system hardening techniques including firewall configuration, SSH hardening, and fail2ban.

## Before Hardening
- Open ports, firewall status, SSH config, and fail2ban status were captured.
- Screenshots are in `before_screenshots/`:

  - `ports_before.png`
  - `ufw_before.png`
  - `ssh_config_before.png`
  - `fail2ban_before.png`

## Hardening Steps
1. Configured UFW firewall:
   - Blocked all incoming connections
   - Allowed all outgoing connections
   - Allowed SSH only
2. Secured SSH server:
   - Disabled root login
   - Disabled password authentication
   - Allowed only user `student`
3. Installed and enabled fail2ban for brute-force attack protection.
4. Verified open ports and service status.

## After Hardening
- Screenshots are in `after_screenshots/`:

  - `ports_after.png`
  - `ufw_after.png`
  - `ssh_config_after.png`
  - `fail2ban_after.png`

- Only necessary ports are open.
- SSH is secure.
- Fail2ban is running.

## Commands Used
See `commands.txt` for a complete list of all commands run during the task.

## Notes
- tcpdump/PCAP capture skipped due to VM network limitations; all other hardening steps are completed.
