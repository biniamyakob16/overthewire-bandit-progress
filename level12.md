# Bandit Level 12

## Objective
- Convert the file containing the password for the next level from hexdump to a binary file.
- Decompress repeatedly until the plaintext password is found.

## Commands Used
```bash
ssh bandit12@bandit.labs.overthewire.org -p 2220
mktemp -d

# Convert hex dump to binary
xxd -r data.txt > newdata.bin

# Decompress layers until ASCII text is found
file newdata.bin			#check file type
mv newdata.bin newdata.gz 	# rename for gzip decompression
gzip -d newdata.gz			# if gzip
bunzip2 newdata				#if bzip2
tar -xf newdata				#if tar archive

# Repeat above steps as needed
```

## Concepts Learned
- A hexdump is a representation of binary data in hexadecimal numbers (0‑9, A‑F)
- 'xxd' is used to create a hex dump from a file or reverse a hex dump back into binary.
- 'file' command is useful to identify compression type (gzip2, bzip2, tar) at each layer.

## Evidence
See screenshot: 
- [screenshots/level12.png](screenshots/level12.png)



