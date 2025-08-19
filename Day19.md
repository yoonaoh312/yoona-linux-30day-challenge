# Day 19: Manage Systemd Services – Start, Stop, Enable, Disable

## 🗓️ Date
2025-08-19

## ✅ Goal
Learn how to manage services on a Linux system using systemctl: starting, stopping, enabling, and disabling services.

## 🗂️ Key Commands and Their Purpose
| Command / Syntax                      | Description                                           |
| ------------------------------------- | ----------------------------------------------------- |
| `systemctl status <service>`          | Check the current status of a service                 |
| `sudo systemctl start <service>`      | Start a service immediately                           |
| `sudo systemctl stop <service>`       | Stop a running service                                |
| `sudo systemctl restart <service>`    | Restart a service                                     |
| `sudo systemctl enable <service>`     | Enable a service to start automatically on boot       |
| `sudo systemctl disable <service>`    | Disable a service from starting automatically on boot |
| `sudo systemctl is-enabled <service>` | Check if a service is enabled at boot                 |
| `journalctl -u <service>`             | View logs related to a specific service               |


## 🔍 What I Did Today
- Checked the status of a service using systemctl status.
- Practiced starting and stopping services (e.g., nginx).
- Enabled services to start automatically on boot.
- Disabled services and verified they don’t start on reboot.
- Used journalctl to view logs and troubleshoot.

#!/bin/bash

# Example service: nginx
SERVICE=nginx

# Check status
systemctl status $SERVICE

# Start the service
sudo systemctl start $SERVICE

# Stop the service
sudo systemctl stop $SERVICE

# Restart the service
sudo systemctl restart $SERVICE

# Enable service on boot
sudo systemctl enable $SERVICE

# Disable service on boot
sudo systemctl disable $SERVICE

# Check if enabled
systemctl is-enabled $SERVICE

# View logs
journalctl -u $SERVICE --no-pager | tail -n 20

## 🧠 Notes
- systemctl is the main tool for controlling systemd services.
- Enabling a service ensures it runs after every reboot.
- Disabling prevents automatic startup but does not stop a running service.
- journalctl is very useful for checking errors and debugging services.
- Always use sudo when managing services to avoid permission issues.