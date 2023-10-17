---
tags:
  - python
---
#### Description

Fix the syntax error in the Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/6/fixme2.py)

>[!hint]- Hint 1
> ASCII is one of the most common encodings used in programming

>[!hint]- Hint 2
> We know that the glitch output is valid Python, somehow!

>[!hint]- Hint 3
> Press Ctrl and c on your keyboard to close your connection and return to the
command prompt.


---

### Step 1
Download the python script using wget on the picoCTF webshell 
```bash
wget https://artifacts.picoctf.net/c/6/fixme2.py
```

### Step 2
try to run the file 
```shell
python fixme2.py 
  File "/home/g2_pilot_tester-picoctf/fixme2.py", line 22
    if flag = "":
       ^^^^^^^^^
SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?
```
using nano change the line 22 to `if flag == "":`


### Flag
> [!question]- Flag
> 







