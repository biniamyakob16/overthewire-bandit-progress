# Bandit Level 4

## Objective
Locate and read the only human-readable file in the inhere directory to obtain the password for the next level.

## Commands Used
```bash
ssh bandit4@bandit.labs.overthewire.org -p 2220
pwd
ls
file -- *
file -- * | grep text
cat -- "special-file-name"
```

## Concepts Learned
- Differentiating human-readable text files from binary files
- Using the file command to determine file types
- Reading files using relative paths
- Safe file access from the shell

## Evidence
See screenshot: 
- [screenshots/level4.png](screenshots/level4.png)



