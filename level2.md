# Bandit Level 2

## Objective
Locate and read a file with spaces in its filename to obtain the password for the next level.

## Commands Used
```bash
ssh bandit1@bandit.labs.overthewire.org -p 2220
pwd
ls
cat -- "special-file-name"
```

## Concepts Learned
- Handling files with special filenames
- Reading files using relative paths
- Safe file access from the shell

## Evidence
See screenshot: 
- [screenshots/level2.png](screenshots/level2.png)



