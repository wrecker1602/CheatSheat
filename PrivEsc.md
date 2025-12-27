# Priv esc stuff
```bash
getcap -r / 2>/dev/null
```
To check for binaries with too much rights that can be run with low rights.
```bash
find / -type f -a \( -perm -u+s -o -perm -g+s \) -exec ls -l {} \; 2> /dev/null
```
Find all files suid and sgid files
