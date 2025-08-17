# Day 17: Permissions Project – Script to Fix Folder Permissions
## 🗓️ Date
2025-08-17

## ✅ Goal
Write a script to automatically fix folder and file permissions for a given project directory.

## 🗂️ Key Commands and Their Purpose
| Command / Syntax                           | Description                                   |
| ------------------------------------------ | --------------------------------------------- |
| `find <dir> -type d -exec chmod 755 {} \;` | Apply 755 permissions to all directories      |
| `find <dir> -type f -exec chmod 644 {} \;` | Apply 644 permissions to all files            |
| `chown -R user:group <dir>`                | Change ownership of all files and folders     |
| `stat -c "%A %n" <file>`                   | Display a file’s permissions in readable form |
| `chmod +x fix_permissions.sh`              | Make the permissions script executable        |
| `./fix_permissions.sh <dir>`               | Run the permissions script                    |

## 🔍 What I Did Today
- Created a script to standardize project directory permissions.
- Applied 755 to directories and 644 to files.
- Ensured correct ownership for all files.
#!/bin/bash
PROJECT_DIR=$1

if [ -z "$PROJECT_DIR" ]; then
    echo "Usage: $0 <project_directory>"
    exit 1
fi

echo "Fixing permissions in $PROJECT_DIR..."

# Set directory permissions
find "$PROJECT_DIR" -type d -exec chmod 755 {} \;

# Set file permissions
find "$PROJECT_DIR" -type f -exec chmod 644 {} \;

# Fix ownership
chown -R $USER:$USER "$PROJECT_DIR"

echo "Permissions fixed successfully!"

## 🧠 Notes
- Standard: directories = 755, files = 644.
- Ownership matters as much as permissions.
- Scripts save time and prevent mistakes when fixing permissions.