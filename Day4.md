# Day 4: System Info Script

## 🗓️ Date
2025-08-02

## ✅ Goal
Create a script to display basic system information, including memory usage, disk space, and CPU details. Learn how to retrieve and format real-time system data using common CLI tools.

## 🗂️ Key Commands and Their Purpose
Command	   Description
- free -h  Displays memory usage in a human-readable format.
- df -h	   Shows disk space usage across mounted filesystems.
- lscpu	   Lists detailed information about the CPU architecture.
- grep	   Filters and extracts specific lines or fields from command output.
- echo -e  Prints formatted text including escape sequences like newlines or emojis.

🔍 What I Did Today
- Wrote a Bash script to display system information:
Used free -h to check total, used, and available memory.
Used df -h to show disk usage in a readable format.
Used lscpu piped with grep to extract key CPU details like model name and core count.
Tested the script in the terminal and added formatting (section titles and emojis).
Made the script executable using chmod +x.
Practiced re-running the script to see updated resource usage after opening/closing programs.

🧪 Sample Output:
bash
Copy
Edit
===== System Info Report =====

🧠 Memory Usage:
              total        used        free      shared  buff/cache   available
Mem:           15Gi       3.2Gi       7.8Gi       654Mi       4.0Gi        11Gi

💾 Disk Usage:
Filesystem      Size  Used Avail Use% Mounted on
/dev/sda1        50G   20G   28G  42% /

🖥️ CPU Info:
Architecture:            x86_64
CPU(s):                  8
Model name:              Intel(R) Core(TM) i7-xxxx

🧠 Notes
- lscpu gives detailed hardware info; grep helps simplify the output.
- free -h and df -h are great for quickly checking system resource availability.
- chmod +x script.sh makes the script executable.
- Consider redirecting output to a file for logging: ./sysinfo.sh > report.txt.

⚠️ Windows PowerShell and Linux/macOS Bash use different system commands:
Task	Linux/macOS (Bash)	Windows (PowerShell)
Memory Usage	free -h	Get-CimInstance Win32_OperatingSystem
Disk Space	df -h	Get-PSDrive -PSProvider FileSystem
CPU Info	lscpu	Get-CimInstance Win32_Processor