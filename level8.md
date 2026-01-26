# Bandit Level 8

## Objective
Locate and read the file containing the password for the next level,where the password is the only line that occurs exactly once in the file.

## Commands Used
```bash
ssh bandit8@bandit.labs.overthewire.org -p 2220
sort data.txt | uniq -u
```

## Concepts Learned
- Using sort to arrange file lines in order
- Using uniq command to filter out unique lines,uniq -u keeps only lines that appear once

## Evidence
See screenshot: 
- [screenshots/level8.png](screenshots/level8.png)



