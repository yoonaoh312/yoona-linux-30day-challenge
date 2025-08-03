# Day 3: File Permissions

## 🗓️ Date
2025-08-01

## ✅ Goal
Understand and manage file permissions using chmod, chown, and ls -l. Learn symbolic and octal notation for permission changes.

## 🗂️ Key Commands and Their Purpose
Command	Description
- ls -l Lists files with detailed permissions, ownership, - and timestamps.
- chmod Changes file permissions (read/write/execute) using symbolic (rwx) or numeric (octal) format.
- chown Changes file or directory ownership (user and/or group).

## 🔍 What I Did Today
- Explored permission details with ls -l:
Saw formats like -rw-r--r-- and learned what each section means (file type, owner/group/others permissions).
- Used chmod to change permissions:
- Symbolic: chmod u+x script.sh (give execute permission to user)
- Octal: chmod 755 file.sh (user: rwx, group: r-x, others: r-x)
- Practiced with permission combinations:
- chmod 644 file.txt (read/write for user, read-only for group/others)
- chmod -R 700 myfolder/ (recursive: full access for user only)
- Changed ownership using chown:
- sudo chown username file.txt (change owner)
- sudo chown username:groupname file.txt (change owner and group)
- Verified changes using ls -l after each command.

## 🧠 Notes
- First character in ls -l output shows file type: - (file), d (directory).
- Permissions are grouped as user (u), group (g), and others (o).
- Octal permission values:
4 = read (r)
2 = write (w)
1 = execute (x)
- Combine for each section (e.g., chmod 764 = user: rwx, group: rw-, others: r--)
- Always be careful with chmod -R and chown -R — they apply changes recursively.

