# Day 10: Process Management – Monitor and Control Processes with ps, top, kill, htop, and nice

## 🗓️ Date  
2025-08-09

## ✅ Goal  
Learn how to view running processes, monitor system performance, terminate processes, and manage process priorities using Linux process management tools.

## 🗂️ Key Commands and Their Purpose  
Command / Syntax                       | Description  
---------------------------------------|---------------------------------------------  
ps aux                                 | Display all running processes with detailed information  
ps -ef                                 | Show processes in full-format listing  
top                                    | Real-time view of running processes and system resource usage  
htop                                   | Interactive process viewer with navigation and search features (requires installation)  
kill <PID>                             | Terminate a process by its Process ID (PID)  
kill -9 <PID>                          | Force terminate a process immediately  
nice -n <priority> <command>           | Start a process with a specific priority (lower value = higher priority)  
renice <priority> -p <PID>             | Change the priority of an already running process  

## 🔍 What I Did Today  
- Viewed all running processes with:
  ```bash
  ps aux

## 🧠 Notes
- ps is great for snapshots of processes; top and htop are for real-time monitoring.
- kill -9 should be a last resort, as it does not allow processes to clean up before exiting.
- Priority values range from -20 (highest priority) to 19 (lowest priority).
- nice sets the priority at process start; renice adjusts it after it’s running.
- Always double-check the PID before killing a process to avoid stopping critical system services.