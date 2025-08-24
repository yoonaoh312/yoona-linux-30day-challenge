# Day 23: Upload Script to GitHub

## 🗓️ Date
2025-08-24

## ✅ Goal
Connect a local Git repository to GitHub and push the first project.

## 🗂️ Key Commands and Their Purpose
| Command / Syntax                                                      | Description                                    |
| --------------------------------------------------------------------- | ---------------------------------------------- |
| git remote add origin https://github.com/username/repo.git            | Add a remote GitHub repository                 |
| git remote -v                                                         | Verify remote repository link                  |
| git branch -M main                                                    | Rename the default branch to `main`            |
| git push -u origin main                                               | Push commits from local `main` to GitHub       |
| git pull origin main                                                  | Pull latest changes from remote repository     |
| ssh-keygen -t rsa -b 4096                                             | Generate SSH key for authentication            |
| cat ~/.ssh/id_rsa.pub                                                 | Display public SSH key to add to GitHub        |

## 🔍 What I Did Today
- Created a new repository on GitHub.  
- Linked my local project to GitHub using `git remote add origin`.  
- Renamed the branch from `master` to `main` for consistency.  
- Pushed the local commits to GitHub with `git push -u origin main`.  
- Verified that the project is now visible on GitHub.  

## 🧠 Notes
- Use HTTPS or SSH to connect to GitHub; SSH is more secure for long-term use.  
- Always check `git remote -v` to ensure the correct GitHub repo is linked.  
- The first push uses `-u` to set the upstream branch, simplifying future pushes.  
- Good practice: add `.gitignore` before pushing to avoid uploading unnecessary files.  