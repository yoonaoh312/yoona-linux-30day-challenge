# Day 5: Disk Usage Script

## 🗓️ Date
2025-08-02

## ✅ Goal
Build a Bash script that lists the largest files and directories in the system using disk usage tools. Learn how to sort and analyze storage consumption efficiently.

## 🗂️ Key Commands and Their Purpose
Command	    Description
- du -ah	Displays disk usage for all files and directories, in human-readable format.
- df -h	    Shows available and used disk space on mounted filesystems.
- sort -rh	Sorts lines by human-readable sizes in reverse order (largest first).
- head -n	Limits output to a specific number of lines.
- echo	    Prints text to the terminal.

## 🔍 What I Did Today
- Created a Bash script to:
Show filesystem usage using df -h
Identify top 10 largest files/directories using du, sort, and head
Learned how to sort files by size using sort -rh
Used head -n 10 to keep the output concise
Saved the output to a .txt file using redirection
Made the script executable with chmod +x
Tested the script by running it in multiple directories

## 🧪 Sample Output
bash
Copy
Edit
===== Disk Usage Report =====

💽 Filesystem Usage:
Filesystem      Size  Used Avail Use% Mounted on
/dev/sda1        50G   20G   28G  42% /

📦 Top 10 Largest Files/Dirs:
1.2G    ./Downloads/movie.mkv
620M    ./node_modules
410M    ./Documents
...
## 🧠 Notes
- Use du -ah in the current directory to see all file sizes recursively.
- sort -rh ensures largest items appear first.
- You can change the number of results by editing head -n 10.
- Redirect script output to a file:
./disk_report.sh > disk_summary.txt

## ⚠️ Windows PowerShell vs Linux/macOS Bash
Task	Linux/macOS (Bash)	Windows (PowerShell)
Disk Space	df -h	Get-PSDrive -PSProvider FileSystem
File Sizes	`du -ah .	sort -rh`
Save Output	> report.txt	Out-File -FilePath report.txt
