# Bandit Level 20

## Objective
- Retrieve the password for Level 21 by using the setuid binary `suconnect` and a netcat listener.

## Commands Used
1. Verify the Setuid binary file:
```bash
ls -l
```
2. Open a second terminal, SSH into bandit20, and set up a listener serving level 20's password:
```bash
echo "level20_password" | nc -lp 1234
```
3. Back in the first terminal, run suconnect with the same port to connect to the listener:
```bash
./suconnect 1234
```

## Concepts Learned
### Localhost
- Refers to your own machine (127.0.0.1).
- The suconnect binary connects back to the same machine it is running on.

## Key Insight
- You are acting as both the server (nc listener) and the client (suconnect) on the same machine.
- Running `./suconnect` without arguments reveals its usage instructions - a good habit when exploring unknown binaries.
- You must set up the netcat listener **before** running suconnect - otherwise the connection fails with "Could not connect".

## Evidence
See screenshot: 
- [screenshots/level20-setuid-binary-verification.png](screenshots/level20-setuid-binary-verification.png)
- [screenshots/level20-listener-setup-&-password-detection.png](screenshots/level20-listener-setup-&-password-detection.png)
- [screenshots/level20-successful-connecting-to-listener-&-sending-password.png](screenshots/level20-successful-connecting-to-listener-&-sending-password.png)
- [screenshots/level20-successful-login-to-level21.png](screenshots/level20-successful-login-to-level21.png)




