# Bandit Level 16

## Objective
- Successfully log in to Level 17 using the private SSH key exposed on the secure port on the Level 16 server.

## Commands Used
1. Scan for open ports
```bash
nmap -p 31000-32000 localhost
```
This scans all ports between 31000-32000 to identify which ones are open.

2. Identify SSL/TLS Services
``` bash
echo "<password>" | openssl s_client -connect localhost:<port> -quiet
```
- Replace <password> with the Level16 password
- Replace <port> with each open port found
This command sends the password to SSL-enabled services and displays their response.

3. Save the Private Key
Copy the returned key and save it locally:
``` bash 
nano bandit17key.txt
```

4. SSH into Level 17
```bash
ssh -i bandit17key.txt bandit17@bandit.labs.overthewire.org -p 2220	
```

## Concepts Learned
- Port Scanning (Nmap): A network utility used to identify open and active ports.
 `-quiet` flag: used to reduce SSL debug output and shows only the server respoonse.

## Key Insight
- It became possible to locate the correct service and extract the SSH private key by combining port scanning (nmap) with SSL probing (openssl s_client)

## Evidence
See screenshot: 
- [screenshots/level16-#1-nmap-scanning.png](screenshots/level16-#1-nmap-scanning.png)
- [screenshots/level16-#2-identifying-ssl-tls-ports.png](screenshots/level16-#2-identifying-ssl-tls-ports.png)
- [screenshots/level16-#3-ssh-private-key-detection.png](screenshots/level16-#3-ssh-private-key-detection.png)
- [screenshots/level16-#4-ssh-private-key-login.png](screenshots/level16-#4-ssh-private-key-login.png)
- [screenshots/level16-#5-successful-ssh-private-key-login.png](screenshots/level16-#5-successful-ssh-private-key-login.png)



