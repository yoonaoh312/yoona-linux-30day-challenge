# Day 22: Git in Linux

## 🗓️ Date
2025-08-23

## ✅ Goal
Install Git on Linux, initialize a local repository, and make the first commits.

## 🗂️ Key Commands and Their Purpose
| Command / Syntax                     | Description                                      |
| ------------------------------------ | ------------------------------------------------ |
| sudo apt install git -y              | Install Git on Debian/Ubuntu                     |
| git --version                        | Check installed Git version                      |
| git config --global user.name "Name" | Set global username for commits                  |
| git config --global user.email "Email"| Set global email for commits                    |
| git init                             | Initialize a new Git repository                  |
| git status                           | Show current repository state                    |
| git add file.txt                     | Stage a single file                              |
| git add .                            | Stage all changes in the directory               |
| git commit -m "message"              | Commit staged files with a message               |
| git log                              | View commit history                              |

## 🔍 What I Did Today
- Installed Git and configured my username and email.  
- Initialized a new repository inside a project directory.  
- Created and edited files, then staged them with `git add`.  
- Made my first commit with a meaningful message.  
- Checked commit history with `git log`.  

## 🧠 Notes
- Every Git repo starts with `git init`.  
- Always configure `user.name` and `user.email` to avoid anonymous commits.  
- Use `git status` often to understand what is staged, unstaged, or untracked.  
- Commit messages should be descriptive and meaningful.  