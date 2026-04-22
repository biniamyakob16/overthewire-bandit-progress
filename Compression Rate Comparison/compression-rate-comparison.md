# Compression Algorithm Comparison (gzip vs bzip2 vs xz)

## Overview

This experiment compares three common compression algorithms — `gzip`, `bzip2`, and `xz` — based on how much disk space they save.

## Test Data

* Original file size: **738,046 bytes**

## Results

| Algorithm | Compressed Size | Space Saved |
| --------- | --------------- | ----------- |
| gzip      | 265,731 bytes   | 64.0%       |
| xz        | 216,064 bytes   | 70.73%      |
| bzip2     | 186,325 bytes   | 74.75%      |

## Analysis

 - bzip2: achieved the highest compression, saving the most space.
 - xz: performed closely behind.
 - gzip: produced the largest output.

## Conclusion
 For this file, bzip2 gave the smallest result,
 
 - bzip2 → smallest file (best compression here)
 - xz → close second
 - gzip → least compression but typically fastest
 
The choice of algorithm depends on whether storage efficiency or performance is the priority.

## Evidence
See screenshot: 

- [screenshots/bzip2-compression.jpg](screenshots/bzip2-compression.jpg)
- [screenshots/xz-compression.jpg](screenshots/xz-compression.jpg)
- [screenshots/gzip-compression.jpg](screenshots/gzip-compression.jpg)







