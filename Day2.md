# Day 2: Basic File Commands

## 🗓️ Date
2025-07-31

## ✅ Goal
Learn how to navigate the filesystem and manage files/directories using basic commands: ls, cd, mkdir, cp, mv, rm and tree.

## 🗂️ Key Directories and Their Purpose
Command	Description
- ls	Lists files and directories in the current directory.
- cd	Changes the current working directory.
- mkdir	Creates a new directory.
- cp	Copies files or directories.
- mv	Moves or renames files/directories.
- rm	Removes files or directories (with -r for folders).
- tree	Displays directory structure in a tree-like format.

## 🔍 What I Did Today
- Used ls to explore folder contents with options:
ls -l, ls -a, ls -lh to see permissions, hidden files, sizes.
- Navigated directories using cd:
Practiced cd ~, cd .., and using absolute/relative paths.
- Created folders with mkdir projects, including nested ones: mkdir -p dev/python.
- Copied files with cp file.txt backup/ and directories using cp -r folder1 folder2.
- Renamed and moved files with mv old.txt new.txt and mv notes.txt docs/.
- Removed files and folders using rm file.txt, rm -r old-folder/.
- Installed and ran tree to visualize directory structure:
sudo apt install tree
tree

## 🧠 Notes
- rm -rf is powerful and dangerous. Be cautious!
- tree helps you understand directory depth quickly.
- Remember: use Tab to autocomplete file/folder names.
- Always double-check the path before using rm or mv.