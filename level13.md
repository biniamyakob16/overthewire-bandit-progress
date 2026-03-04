# Bandit Level 13

## Objective
- Successfully log in to level 14 using the private SSH key provided on the level 13 server.

## Commands Used
```bash
ssh bandit13@bandit.labs.overthewire.org -p 2220
scp -P 2220 bandit13@bandit.labs.overthewire.org:/home/bandit13/sshkey.private ~/Desktop/bandit14_key
chmod u=rw,go= ~/Desktop/bandit14_key
ssh -i ~/Desktop/bandit14_key bandit14@bandit.labs.overthewire.org -p 2220
```

## Concepts Learned
- Secure Copy (SCP) is a command line tool that copies files between systems using SSH for encrypted transport.
- The `-i` option in SSH specifies a private key file for authentication instead of password-based authentication.
- SSH private keys must have restrictive permissions (e.g., 600 or u=rw) to be accepted by the SSH client.

## Evidence
See screenshot: 
- [screenshots/level13.png](screenshots/level13.png)
- [screenshots/level13-ssh-private-key-login.png](screenshots/level13-ssh-private-key-login.png)
- [screenshots/level13-successful-ssh-private-key-login.png](screenshots/level13-successful-ssh-private-key-login.png)

