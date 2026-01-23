# Bandit Level 3

## Objective
Locate and read a hidden file to obtain the password for the next level.

## Commands Used
```bash
ssh bandit3@bandit.labs.overthewire.org -p 2220
pwd
ls -la
cat .hiddenfile
```

## Concepts Learned
- Handling hidden files(files starting with.)
- Using ls -la to list all files,including hidden ones
- Reading files using relative paths
- Safe file access from the shell

## Evidence
See screenshot: 
- [screenshots/level3.png](screenshots/level3.png)



