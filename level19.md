# Bandit Level 19

## Objective
- Get the password for Level 20 from `/etc/bandit_pass/` using the provided setuid binary.

## Commands Used
1. Verify the Setuid binary file
```bash
ls -l bandit20-do
```
2. Execute the setuid binary to read the password file:
```bash
./bandit20-do cat /etc/bandit_pass/bandit20
```

## Concepts Learned
### Setuid Binary
- A setuid (Set User ID) binary is an executable that runs with the privileges of its owner, not the user executing it.
- Indicated by an `s` in the owner execute position (e.g. -rwsr-x---).
- Allows users to perform actions they normally do not have permission to execute.

### Privilege Escalation
- This level demonstrates controlled privilege escalation, where a user temporarily gains elevated access via a trusted binary.

## Key Insight
- The password file `/etc/bandit_pass/bandit20` is not readable by bandit19.
- However, the `bandit20-do` binary runs commands with the privileges of `bandit20`
- By passing `cat /etc/bandit_pass/bandit20` as an argument, the file is read with the correct permissions.

## Evidence
See screenshot: 
- [screenshots/level19-setuid-binary-verification.png](screenshots/level19-setuid-binary-verification.png)
- [screenshots/level19-permission-denial.png](screenshots/level19-permission-denial.png)
- [screenshots/level19-password-detection.png](screenshots/level19-password-detection.png)
- [screenshots/level19-successful-login-to-level20.png](screenshots/level19-successful-login-to-level20.png)




