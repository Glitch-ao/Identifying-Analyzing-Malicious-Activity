# Identifying & Analyzing Malicious Activity

This project focuses on detecting unauthorized privilege escalation and analyzing system behavior through resource utilization and auditing logs. I worked with tools on both Windows and Linux platforms to monitor user actions, generate audit logs, and flag suspicious activity.

## Tags
`Resource Utilization` `User Privilege Monitoring` `Auditing Logs` `Privilege Escalation`

---

### 1. Resource Utilization Monitoring
- **Windows**: Used **Task Manager**, **Resource Monitor**, and `Get-Process` in PowerShell to analyze CPU, memory, and disk usage.
- **Linux**: Monitored active processes and system resources with commands like `top`, `htop`, `vmstat`, and `iotop`.

### 2. User Privilege Monitoring
- Enabled **Audit Policy** settings via `secpol.msc` on Windows to track privilege use and account management events.
- Used `auditctl` and `ausearch` on Linux to track `sudo` activity and privilege elevation attempts.

### 3. Audit Log Configuration and Generation
- Configured **audit logging** on Windows using Group Policy to generate logs for logon attempts, privilege changes, and object access.
- On Linux, edited `/etc/audit/audit.rules` to log sensitive commands and access to `/etc/sudoers`, `/etc/passwd`, and critical system binaries.

### 4. Detecting Unauthorized Privilege Escalation
- Simulated privilege escalation attempts using:
  - `runas` on Windows
  - `sudo` misuse and modified SUID binaries on Linux
- Analyzed **Event Viewer** and **audit logs** for Event IDs (e.g., 4672 – Special privileges assigned, 4688 – New process creation).
- Correlated log data with resource spikes and anomalous user activity.

---

## Learning Outcomes

By the end of this project, I was able to:

- Monitor and analyze system resource usage on both Windows and Linux
- Enable and configure audit logging for user activities
- Track and detect unauthorized user privilege escalation attempts
- Correlate unusual resource usage with suspicious user behavior
- Use built-in tools to collect and review forensic log evidence

---

## Tools & Commands Used

### Windows
- `Task Manager`, `Resource Monitor`, `Event Viewer`
- PowerShell (`Get-Process`, `Get-WinEvent`)
- Local Security Policy (`secpol.msc`)
- Event IDs: 4672, 4688, 4648

### Linux
- `top`, `htop`, `vmstat`, `auditctl`, `ausearch`
- Audit logs: `/var/log/auth.log`, `/var/log/audit/audit.log`

---

## Screenshots
*(Include screenshots of Windows Event Viewer, Linux audit logs, and system monitoring tools in action)*


