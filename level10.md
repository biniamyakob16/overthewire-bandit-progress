# Bandit Level 10

## Objective
- Locate and read the file containing the password for the next level.
- Decode the Base64-encoded contents of `data.txt` to retrieve the plaintext password.

## Commands Used
```bash
ssh bandit10@bandit.labs.overthewire.org -p 2220
base64 --decode data.txt

```

## Concepts Learned
- Base64 is a way of converting binary data into ASCII-safe text using 64 characters (A-Z, a-z, 0-9, +, /).
- Attempting to use `cat data.txt` produces a long ASCII string ending in `=` characters.
- Decoding restores the original plaintext password.
- The file content was not encrypted, only encoded.

## Evidence
See screenshot: 
- [screenshots/level10.png](screenshots/level10.png)



