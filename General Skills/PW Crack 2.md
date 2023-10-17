---
tags:
  - python
  - password_cracking
---
#### Description

Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/14/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/14/level2.flag.txt.enc) in the same directory too.

> [!hint]- Hint 1
> Does that encoding look familiar?
> 

> [!hint]- Hint 2
> The `str_xor` function does not need to be reverse engineered for this challenge.


---

### Step 1
When looking at the password checker file we see the line `if( user_pw == chr(0x35) + chr(0x39) + chr(0x30) + chr(0x39) ):` . We can do the same thing we did in [[Glitch Cat]] and use the python interpreter to get find out what the correct value should be. 
```python
>>> chr(0x35) + chr(0x39) + chr(0x30) + chr(0x39)
'5909'
```
we can now run the password checker and provide it the correct password.
```yaml
Please enter correct password for flag: 5909
Welcome back... your flag, user:
picoCTF{tr******************96}
```


### Flag
> [!question]- Flag
> picoCTF{tr45h_51ng1ng_b0539d96}







