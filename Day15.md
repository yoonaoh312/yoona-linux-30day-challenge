# Day 15: Bash Menu Tool – Build a Menu Script

## 🗓️ Date  
2025-08-15  

## ✅ Goal  
Build a menu-driven Bash script that performs system tasks: update, clean, and show reports.

## 🗂️ Key Commands and Their Purpose  
| Command / Syntax                         | Description |
|------------------------------------------|-------------|
| `echo "text"`                            | Display text to the terminal |
| `read -p "Prompt" var`                   | Accept user input and store it in a variable |
| `case $var in ... esac`                  | Execute different actions based on input |
| `sudo apt update && sudo apt upgrade -y` | Update and upgrade packages |
| `sudo apt autoremove && sudo apt clean`  | Remove unnecessary packages and clean cache |
| `df -h`                                  | Show disk usage in human-readable format |
| `uptime`                                 | Show system uptime |
| `chmod +x script.sh`                     | Make a script executable |
| `./script.sh`                            | Run the script |

## 🔍 What I Did Today  
- Created a Bash menu tool script with multiple options.  
- Script handles system updates, cleaning, and showing reports.  
- Used `case` to handle menu selections.  

```bash
#!/bin/bash
while true; do
    echo "===== System Menu ====="
    echo "1) Update System"
    echo "2) Clean System"
    echo "3) Show Report"
    echo "4) Exit"
    read -p "Choose an option: " choice

    case $choice in
        1) sudo apt update && sudo apt upgrade -y ;;
        2) sudo apt autoremove && sudo apt clean ;;
        3) echo "=== System Report ==="
           df -h
           uptime ;;
        4) echo "Goodbye!"; exit 0 ;;
        *) echo "Invalid choice!" ;;
    esac
done

## 🧠 Notes

- Menus make repetitive tasks easier to run.
- case is cleaner than long if-else chains.
- Always give scripts execute permission before running.
