# Bandit Level 5

## Objective
Locate and read a human-readable file that is not executable and has a specific size in order to obtain the password for the next level.

## Commands Used
```bash
ssh bandit5@bandit.labs.overthewire.org -p 2220
pwd
ls
cd inhere
find . -type f -size 1033c
cat maybehere07/.file2


```

## Concepts Learned
- Recursively searching directories with find
- Filtering files by exact byte size
- Identifying human-readable files using the file command

## Evidence
See screenshot: 
- [screenshots/level5.png](screenshots/level5.png)



