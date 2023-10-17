---
tags:
  - grep
  - Linux-Commands
---
# Big Zip
---
### Description
---
Unzip this archive and find the flag.

- [Download zip file](https://artifacts.picoctf.net/c/505/big-zip-files.zip)
### Hints
---

> [!hint]- Hint(s)
> 1. Can grep be instructed to look at every file in a directory and its subdirectories?

### Step(s)
---
```
grep -nr 'picoCTF*' .
```

The dot at the end searches the current directory. Meaning for each parameter:

```
-n            Show relative line number in the file
'yourString*' String for search, followed by a wildcard character
-r            Recursively search subdirectories listed
.             Directory for search (current directory)
```
### Flag
---
> [!question]- Flag
> picoCTF{gr3p_15_m4g1c_ef8790dc}







