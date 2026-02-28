# Bandit Level 11

## Objective
- Decode the ROT13-encoded contents of `data.txt` to retrieve the plaintext password for the next level.
- Locate and read the file containing the password for the next level.
- Use ROT 13 substitution cipher to substitute all uppercase(A-Z) & lowercase(a-z) to extract the password .

## Commands Used
```bash
ssh bandit11@bandit.labs.overthewire.org -p 2220
tr 'A-Za-z' 'N-ZA-Mn-za-m' < data.txt
```

## Concepts Learned
- ROT13 is a Caesar cipher variant that shifts letters 13 positions forward.
- 'tr' performs character-by-character positional substitution.
- Attempting to use `cat data.txt` reveals a readable but not the actual plaintext password. a wrong password string.

## Evidence
See screenshot: 
- [screenshots/level11.png](screenshots/level11.png)



