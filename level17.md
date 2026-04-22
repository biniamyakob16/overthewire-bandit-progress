# Bandit Level 17

## Objective
- Retrieve the password for Level 18 by identifying the unique line present in `passwords.new`

## Commands Used
1. Compare both files and extract the line unique to `passwords.new`	
```bash
comm -13 <(sort passwords.old) <(sort passwords.new)
```
- `-1`: suppress lines unique to first file (`passwords.old`)
- `-3`: suppress lines common to both
→ Result: shows only lines unique to `passwords.new`

## Concepts Learned
- `comm` : compares two sorted files line by line and outputs three columns:
- Column 1: lines only in first file
- Column 2: lines only in second file
- Column 3: lines common to both


## Key Insight
- The password is the only line that differs between the two files.
- By suppressing common lines and those unique to `passwords.old`, `comm -13` isolates the new password directly.
- Note: `comm` requires both files to be sorted.


## Evidence
See screenshot: 
- [screenshots/level17-password-detection.png](screenshots/level17-password-detection.png)
- [screenshots/level17-successful-login.png](screenshots/level17-successful-login.png)



