---
tags:
  - python
---
#### Description

Fix the syntax error in this Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/25/fixme1.py)

> [!hint]- Hint 1
>Indentation is very meaningful in Python

> [!hint]- Hint 2
> To view the file in the webshell, do: `$ nano fixme1.py`

> [!hint]- Hint 3
> To exit `nano`, press Ctrl and x and follow the on-screen prompts.

> [!hint]- Hint 4
> The `str_xor` function does not need to be reverse engineered for this challenge.


---

### Step 1
using wget download the file onto the picoCTF Webshell
```bash
wget https://artifacts.picoctf.net/c/25/fixme1.py
```

### Step 2
try to run the file 
```bash
python fixme1.py 
  File "/home/g2_pilot_tester-picoctf/fixme1.py", line 20
    print('That is correct! Here\'s your flag: ' + flag)
IndentationError: unexpected indent
```
Seeing the Indentation error this means that line 20  indentation needs to get fixed. you can fix it with nano and rerun the file to get the flag.

### Flag
> [!question]- Flag
> picoCTF{1nd3nt1ty_cr1515_6a476c8f}







