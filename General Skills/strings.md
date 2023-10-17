---
tags:
  - strings
  - Linux-Commands
---
#### Description

Can you find the flag in file without running it?

> [!hint]- Hint
>[strings](https://linux.die.net/man/1/strings)

---

### Step 1
1. Download the file from picoCTF
2. run `strings -d /strings | grep pico`
3. This command will get all of the data from the file strings then will grep out the line that has pico in it.


### Flag
> [!question]- Flag
> picoCTF{5tRIng5_1T_827aee91}







