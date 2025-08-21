# Day 20: Create and Manage Custom Systemd Service

## 🗓️ Date
2025-08-20

## ✅ Goal
Learn how to create, configure, and manage a custom systemd service using a unit file.  

## 🗂️ Key Commands and Their Purpose
| Command / Syntax                              | Description                                           |
| --------------------------------------------- | ----------------------------------------------------- |
| `sudo nano /etc/systemd/system/<service>.service` | Create or edit a custom service unit file             |
| `sudo systemctl daemon-reload`                | Reload systemd manager configuration after changes    |
| `sudo systemctl start <service>`              | Start the custom service                              |
| `sudo systemctl stop <service>`               | Stop the custom service                               |
| `sudo systemctl enable <service>`             | Enable the service to run at boot                     |
| `sudo systemctl disable <service>`            | Disable the service from running at boot              |
| `systemctl status <service>`                  | Check the current status of the custom service        |
| `journalctl -u <service>`                     | View logs for the custom service                      |

## 🔍 What I Did Today
- Created a simple shell script (`hello.sh`) that writes a log entry every minute.  
- Built a custom systemd service unit file (`hello.service`).  
- Reloaded systemd so it recognizes the new service.  
- Started and stopped the service using `systemctl`.  
- Enabled the service to run automatically at boot.  
- Checked logs with `journalctl` to confirm service activity.  

```bash
#!/bin/bash
while true; do
  echo "Hello from systemd service at $(date)" >> /home/yoona312/hello.log
  sleep 60
done


# File: /etc/systemd/system/hello.service
[Unit]
Description=Simple Hello Service
After=network.target

[Service]
ExecStart=/usr/local/bin/hello.sh
Restart=always

[Install]
WantedBy=multi-user.target

# Reload systemd to recognize new service
sudo systemctl daemon-reload

# Start the service
sudo systemctl start hello.service

# Check status
systemctl status hello.service

# Enable service on boot
sudo systemctl enable hello.service

# Disable service
sudo systemctl disable hello.service

# View logs
journalctl -u hello.service --no-pager | tail -n 20

## 🧠 Notes
- Custom services are defined in /etc/systemd/system/.
- Always run sudo systemctl daemon-reload after editing or creating a unit file.
- The [Install] section defines when the service starts automatically.
- Using Restart=always ensures the service restarts if it crashes.
- Logs can be tracked in /var/log/ or with journalctl.