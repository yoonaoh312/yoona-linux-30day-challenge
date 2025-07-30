# Day 1: Linux Directory Structure

## 🗓️ Date
2025-07-30

## ✅ Goal
Understand the purpose of the major Linux directories.

## 🗂️ Key Directories and Their Purpose

| Directory | Description |
|----------|-------------|
| `/home`  | User home directories (e.g. /home/yoona) |
| `/etc`   | System configuration files |
| `/var`   | Variable data like logs and spools |
| `/bin`   | Essential command binaries (e.g. `ls`, `cp`) |
| `/usr`   | Secondary hierarchy for user applications |
| `/sbin`  | System binaries (used by root) |
| `/tmp`   | Temporary files, cleared on reboot |
| `/root`  | Root user’s home directory |
| `/dev`   | Device files (e.g. hard drives) |
| `/proc`  | Virtual filesystem with process/system info |
| `/lib`   | Shared libraries for binaries in `/bin` and `/sbin` |

## 🔍 What I Did Today
- Used `ls`, `cd`, `file`, and `head` to explore each directory.
- Noticed that:
  - `/etc` contains many `.conf` files.
  - `/var/log` has logs like `syslog` and `auth.log`.
  - `/proc` looks strange—virtual files related to running processes.
- Learned the difference between `/bin` and `/usr/bin`.