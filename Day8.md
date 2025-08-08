# Day 8: Cron Jobs – Automate a Task Using Crontab

## 🗓️ Date  
2025-08-07

## ✅ Goal  
Learn how to automate tasks using `cron` and `crontab`. Understand how to write a shell script and schedule it to run automatically at a specified time.

## 🗂️ Key Commands and Their Purpose  
Command / Syntax                      | Description  
-------------------------------------|---------------------------------------------  
`crontab -e`                         | Open the crontab file for editing.  
`* * * * * /path/to/script.sh`       | Cron syntax to run a script every minute.  
`crontab -l`                         | List current user's cron jobs.  
`crontab -r`                         | Remove all cron jobs (use with caution).  
`chmod +x script.sh`                 | Make a script executable.  
`date`                               | Print the current system date and time.  
`echo "text" >> file.txt`            | Append text to a file.

## 🔍 What I Did Today  
- Created a shell script using `vi log_time.sh`:
  ```bash
  #!/bin/bash
  echo "Current time: $(date)" >> /home/ec2-user/time_log.txt

## 🧠 Notes  
- `cron` runs in the background and is separate from your logged-in shell session.  
- `crontab -e` edits cron jobs for the current user only.  
- You **must use full (absolute) paths** in cron jobs (e.g., `/home/ec2-user/...`) — relative paths usually don’t work.  
- The cron environment has a **limited $PATH**, so common commands like `python` or `node` may not work unless given with full paths (e.g., `/usr/bin/python3`).  
- Always make your script executable with `chmod +x script.sh`.  
- You can log output and errors using:
  ```bash
  * * * * * /path/to/script.sh >> /path/to/output.log 2>&1
