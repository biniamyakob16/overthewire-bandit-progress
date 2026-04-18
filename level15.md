# Bandit Level 15

## Objective
- Retrieve the password for the next level by submitting the current level's password to port 30001 on localhost using SSL/TLS encryption.

## Commands Used
## Steps
1. Connect to the service:
```bash
openssl s_client -connect localhost:30001
```
2. Wait for the SSL handshake to complete.
3. Paste the password for level 15.
4. Press Enter to receive the password for level 16.

## Concepts Learned
- OpenSSL: A toolkit used for implementing SSL/TLS protocols.
- The `s_client` command allows to establish a secure, encrypted connection to a server.

## Key Insight
- The service on port 30001 requires an SSL/TLS encrypted connection.
- Using `nc` fails because it creates an unencrypted connection.
- The server expects encrypted communication,so it ignores plain-text input.
- `openssl s_client` performs the SSL/TLS handshake, allowing communication with the server.

## Evidence
See screenshot: 
- [screenshots/level15-ssl-tls-encryption-login.png](screenshots/level15-ssl-tls-encryption-login.png)
- [screenshots/level15-successful-ssl-tls-encryption-login.png](screenshots/level15-successful-ssl-tls-encryption-login.png)
