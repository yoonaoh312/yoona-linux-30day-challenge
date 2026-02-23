# Day 25: Watch a Directory with inotifywait

## 🗓️ Date
2026-02-22

## ✅ Goal
Monitor a directory for file changes (creation, modification, deletion) in real-time using inotifywait from the inotify-tools package.

## 🗂️ Key Commands and Their Purpose
| Command / Syntax                           | Description                                               |
| ------------------------------------------ | --------------------------------------------------------- |
| `#!/bin/bash`                              | Define the script as a Bash script                        |
| `sudo apt install inotify-tools`           | Install the inotifywait tool on Debian/Ubuntu             |
| `inotifywait -m /path/to/dir`              | Monitor the specified directory continuously              |
| `-e create`, `-e modify`, `-e delete`      | Specify events to watch: creation, modification, deletion |
| `--format '%w%f %e'`                       | Customize output to show file path and event type         |
| `while read path action file; do ... done` | Loop to process events as they occur                      |
| `echo`                                     | Print the detected event and file path to terminal        |
| `chmod +x script.sh`                       | Make your Bash script executable                          |
| `./script.sh`                              | Run your Bash script                                      |

🔍 What I Did Today
- Installed inotify-tools to get inotifywait.
- Created a Bash script named watch_dir.sh.
- Used inotifywait -m to monitor a specific directory continuously.
- Specified events to watch: create, modify, and delete.
- Added a loop to process each event as it occurs.
- Formatted output to show which file changed and what action occurred.
- Tested by creating, editing, and deleting files in the monitored directory.
- Observed real-time detection of events in the terminal.

## 🧠 Notes
- inotifywait -m runs indefinitely until you stop it with Ctrl+C.
- Can watch multiple directories at once by listing them after inotifywait.
- Useful for automation: trigger scripts whenever files change.
- Great for monitoring logs, configuration files, or development directories.
- Always check permissions; inotifywait needs access to the directory.