# Day 16: Set up SSH Server – Enable SSH, Configure, Test Login

## 🗓️ Date
2025-08-16

## ✅ Goal
Install and configure an SSH server to allow secure remote logins and test it from a client machine.

## 🗂️ Key Commands and Their Purpose
| Command / Syntax                         | Description |
|------------------------------------------|-------------|
| `sudo apt install openssh-server -y`     | Install OpenSSH server |
| `sudo systemctl enable ssh`              | Enable SSH service at boot |
| `sudo systemctl start ssh`               | Start SSH service |
| `sudo systemctl status ssh`              | Check SSH service status |
| `ip a`                                   | Show system IP address |
| `ssh user@IP_address`                    | Connect to a server via SSH |
| `ssh-keygen -t ed25519`                  | Generate an SSH key pair on client |
| `ssh-copy-id user@IP_address`            | Copy public key to server |
| `sudo nano /etc/ssh/sshd_config`         | Edit SSH configuration file |
| `sudo systemctl restart ssh`             | Restart SSH after configuration changes |

## 🔍 What I Did Today
- Installed the OpenSSH server package.
- Enabled and started the SSH service.
- Checked server IP using ip a.
- Generated an SSH key on the client machine and copied it to the server.
- Successfully logged in remotely using:
ssh myuser@192.168.1.100
- Edited /etc/ssh/sshd_config to improve security (disable root login, allow key-based login only).

## 🧠 Notes
SSH provides encrypted remote access.
Prefer SSH keys over passwords.
Update firewall rules if changing the default SSH port (sudo ufw allow <port>/tcp).