# Bandit Level 14

## Objective
- Retrieve the password for the next level by submitting the current level's password to port 30000 on localhost.

## Commands Used
```bash
cat /etc/bandit_pass/bandit14
nc localhost 30000
```

## Concepts Learned
- Netcat (nc): A networking utility used to read from and write to raw network connections over TCP/UDP.
- Localhost (127.0.0.1): Refers to the current machine itself.

## Evidence
See screenshot: 
- [screenshots/level14.png](screenshots/level14.png)
