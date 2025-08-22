# Day 21: Archive & Compress

## 🗓️ Date
2025-08-21

## ✅ Goal
Learn how to archive and compress files using tar, zip, gzip, xz and automate the process with a simple shell script.

## 🗂️ Key Commands and Their Purpose
| Command / Syntax                              | Description                                           |
| --------------------------------------------- | ----------------------------------------------------- |
| tar -cvf archive.tar /path/to/files           | Create a .tar archive from files or directories      |
| tar -xvf archive.tar                           | Extract files from a .tar archive                    |
| tar -czvf archive.tar.gz /path/to/files       | Create a compressed .tar.gz archive using gzip       |
| tar -xvzf archive.tar.gz                       | Extract a .tar.gz archive                             |
| tar -cJvf archive.tar.xz /path/to/files      | Create a compressed .tar.xz archive using xz         |
| tar -xvJf archive.tar.xz                       | Extract a .tar.xz archive                             |
| zip archive.zip file1 file2                    | Create a zip archive                                  |
| unzip archive.zip                              | Extract a zip archive                                 |
| gzip file                                     | Compress a file using gzip (creates file.gz)         |
| gunzip file.gz                                 | Decompress a gzip file                                 |
| xz file                                       | Compress a file using xz (creates file.xz)           |
| unxz file.xz                                   | Decompress an xz file                                 |
| crontab -e                                     | Edit cron jobs to automate scripts                   |

## 🔍 What I Did Today
- Learned to create .tar, .tar.gz, .tar.xz, and .zip archives.
- Practiced extracting archives with the correct commands.
- Compressed individual files with gzip and xz and decompressed them.
- Created a simple shell script to automate weekly backup of a directory.
- Tested automation using cron to schedule the backup script.

# Archive and compress with tar and gzip
tar -cvf project_backup.tar /home/yoona312/project
tar -czvf project_backup.tar.gz /home/yoona312/project
tar -cJvf project_backup.tar.xz /home/yoona312/project

# Extract archives
tar -xvf project_backup.tar
tar -xvzf project_backup.tar.gz
tar -xvJf project_backup.tar.xz

# Zip and unzip
zip project_backup.zip /home/yoona312/project/*
unzip project_backup.zip -d /home/yoona312/project_unzip

# Compress and decompress single files
gzip notes.txt
gunzip notes.txt.gz
xz notes.txt
unxz notes.txt.xz

# Example: automate backup with a script
#!/bin/bash
BACKUP_DIR="/home/yoona312/project"
ARCHIVE_DIR="/home/yoona312/backups"
DATE=$(date +%Y-%m-%d)
tar -czvf $ARCHIVE_DIR/project_backup_$DATE.tar.gz $BACKUP_DIR

# Add cron job to run backup every Sunday at 2am
# Edit crontab: crontab -e
0 2 * * 0 /home/yoona312/backup_project.sh

## 🧠 Notes
- tar is primarily for archiving; compression requires -z for gzip or -J for xz.
- zip combines archiving and compression in one command.
- gzip and xz compress individual files only.
- Automating with cron allows repetitive tasks to run without manual intervention.
- Always check permissions and paths when automating scripts.