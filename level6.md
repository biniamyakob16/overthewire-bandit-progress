# Bandit Level 6

## Objective
Locate and read a file on the server that is owned by the user `bandit7` and has a specific size in order to obtain the password for the next level.

## Commands Used
```bash
ssh bandit6@bandit.labs.overthewire.org -p 2220
cd /
find . -type f -user bandit7 -size 33c 2>/dev/null
cat ./var/lib/dpkg/info/bandit7.password 
```

## Concepts Learned
- Recursively searching directories with find
- Filtering files by owner using -user
- Filtering files by exact byte size using -size
- Redirecting error output to the bit bucket (/dev/null) to suppress permission errors

## Evidence
See screenshot: 
- [screenshots/level6.png](screenshots/level6.png)



