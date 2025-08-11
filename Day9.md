# Day 9: Create Users and Groups – Manage Users with useradd, passwd, groupadd, and id

## 🗓️ Date  
2025-08-08

## ✅ Goal  
Learn how to create users and groups on Linux, set user passwords, and check user and group information using command-line tools.

## 🗂️ Key Commands and Their Purpose  
Command / Syntax                     | Description  
-----------------------------------|---------------------------------------------  
sudo groupadd <groupname>           | Create a new user group  
sudo useradd -m -g <group> <user>  | Create a new user with home directory and assign to a primary group  
sudo passwd <user>                  | Set or change the password for a user  
id <user>                         | Display user ID, group ID, and group memberships  
groups <user>                     | Show all groups a user belongs to  

## 🔍 What I Did Today  
- Created a new group `devteam`:
  ```bash
  sudo groupadd devteam

🧠 Notes
- Use sudo to run commands with the right permissions
- -m flag creates user home directory
- -g sets primary group; add secondary groups with -G option
- Password must meet system security rules
- Use id or groups to verify user and group info
- Double-check group and user names to avoid conflicts