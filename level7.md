# Bandit Level 7

## Objective
Locate and read the file containing the password for the next level,which appears immediately after a specific keyword in the text.

## Commands Used
```bash
ssh bandit7@bandit.labs.overthewire.org -p 2220
cat data.txt  | grep millionth
```

## Concepts Learned
- Using grep to search for specific text patterns inside a file
- Piping command output to filter results

## Evidence
See screenshot: 
- [screenshots/level7.png](screenshots/level7.png)



