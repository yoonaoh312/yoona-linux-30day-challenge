# Day 6: Package Management

## 🗓️ Date
2025-08-04

## ✅ Goal
Learn to manage software packages using different package managers: apt, yum, dnf, apt-cache, and dpkg -l. Understand how to install, remove, update, and search for packages.

## 🗂️ Key Commands and Their Purpose
Command	                Description
apt update	            Updates the list of available packages and their versions.
apt upgrade	            Installs the newest versions of all packages currently installed.
apt install	            Installs a new package (e.g., apt install curl).
apt remove	            Removes a package without deleting configuration files.
apt purge	            Removes a package and its configuration files.
apt-cache search	    Searches for a package by keyword.
dpkg -l	                Lists all installed packages on a Debian-based system.
yum install	            Installs a package (Red Hat/CentOS systems).
dnf install	            Replaces yum in newer Fedora/Red Hat systems to install packages.
yum remove / dnf remove	Removes a package from the system.

## 🔍 What I Did Today
- Ran apt update and apt upgrade to ensure the system was current.
- Installed test packages like htop and curl using apt install.
- Removed them using apt remove and practiced cleanup with apt purge.
- Searched for packages with apt-cache search, e.g., apt-cache search python.
- Used dpkg -l to view a list of all installed packages and their versions.
- Explored yum and dnf commands on CentOS and Fedora-based virtual machines.
- Compared syntax and behavior differences between apt and yum/dnf.

## 🧠 Notes
- apt is used on Debian/Ubuntu-based systems, while yum and dnf are for Red Hat/Fedora/CentOS.
- dnf is the modern replacement for yum and handles dependencies better.
- dpkg is a low-level package manager for .deb packages and useful for listing installed packages.
- Be cautious with purge and remove — purge deletes all related configs.
- Use sudo for all package management commands to avoid permission issues.