# Bandit Level 18

## Objective
- Get the password for Level 19 from the readme file even though normal SSH login keeps failing

## Commands Used
1. Run a command directly instead of trying to login
```bash
ssh bandit18@bandit.labs.overthewire.org -p 2220 cat readme
```

## Concepts Learned
- Commands can be executed directly during SSH connection
- Files like `.bashrc` can control what happens right after login


## Key Insight
- At first, it looked like a password issue because I kept getting logged out with a "bye bye" message
- But the real problem was the login process itself, the shell was setup to immediately exit

## Evidence
See screenshot: 
- [screenshots/level18-password-detection.png](screenshots/level18-password-detection.png)
- [screenshots/level18-successful-login-to-level19.png](screenshots/level18-successful-login-to-level19.png)



