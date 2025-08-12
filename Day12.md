# Day 12: File Search – find, locate, which, whereis, grep  

## 🗓️ Date  
2025-08-11  

## ✅ Goal  
Learn how to search for files, locate executables, find command paths, and search within files using essential Linux search commands.  

## 🗂️ Key Commands and Their Purpose  
| Command / Syntax               | Description |
|--------------------------------|-------------|
| find <path> -name "<filename>" | Search for files or directories starting from a specified path |
| find <path> -type f -size +1M   | Find files of a specific type and size |
| locate <filename>              | Quickly search for files using a prebuilt index (requires updatedb) |
| which <command>                 | Show the path of an executable command in the current PATH |
| whereis <command>               | Locate binary, source, and man page files for a command |
| grep "<pattern>" <file>         | Search for text patterns inside files |
| grep -r "<pattern>" <directory> | Search recursively for a pattern in a directory |

## 🔍 What I Did Today  
- Searched for a file named `notes.txt` starting from the home directory:  
  ```bash
  find ~ -name "notes.txt"

## 🧠 Notes
- find searches in real-time, making it slower but always accurate.
- locate is faster but depends on the updated index from updatedb.
- which only looks in directories defined in your PATH, while whereis can show more locations (binary, source, man page).
- grep is powerful for searching inside files; use -i for case-insensitive search, and -n to show line numbers.