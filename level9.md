# Bandit Level 9

## Objective
Locate and read the file containing the password for the next level, where the password is one of the few human-readable strings, preceded by several '=' characters.

## Commands Used
```bash
ssh bandit9@bandit.labs.overthewire.org -p 2220
strings data.txt  | grep "===="
```

## Concepts Learned
- Using `strings` command to extract human-readable text from any file which contains binary/mixed data.
- Attempting to use `cat data.txt` produces unreadable output because the file contains mostly binary data.

## Evidence
See screenshot: 
- [screenshots/level9.png](screenshots/level9.png)



