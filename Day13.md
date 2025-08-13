# Day 13: Log Monitoring – tail, journalctl, less, grep for "error"

## 🗓️ Date  
2025-08-12  

## ✅ Goal  
Learn how to monitor and read system logs, track real-time updates, and filter for specific patterns like errors using Linux log commands.  

## 🗂️ Key Commands and Their Purpose  
| Command / Syntax                         | Description |
|------------------------------------------|-------------|
| `tail -f <logfile>`                      | Monitor a log file in real-time, showing new lines as they are added |
| `tail -n 50 <logfile>`                   | Show the last 50 lines of a log file |
| `journalctl`                             | View system logs managed by systemd |
| `journalctl -u <service>`                | View logs for a specific service |
| `journalctl -f`                          | Follow logs in real-time, similar to `tail -f` |
| `less <logfile>`                         | View long log files page by page |
| `grep "error" <logfile>`                 | Search for the keyword "error" in a log file |
| `journalctl | grep "error"`              | Search for "error" in journalctl logs |
| `grep -i "error" <logfile>`              | Case-insensitive search for "error" |

## 🔍 What I Did Today  
- Monitored a log file in real-time to catch new errors as they occurred:  
```bash
tail -f /var/log/syslog
grep -i "error" /var/log/syslog
journalctl -u nginx.service -f

## 🧠 Notes
- tail -f and journalctl -f are essential for real-time monitoring.
- less is helpful for navigating large log files without loading everything at once.
- grep is powerful for filtering logs; combine with -i for case-insensitive search or -r to search recursively.
- Using journalctl -u <service> helps narrow down issues to a specific service instead of sifting through all logs.
