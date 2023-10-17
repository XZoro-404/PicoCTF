---
tags:
  - python
  - password_cracking
---
#### Description

Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/18/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/18/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/18/level3.hash.bin) in the same directory too.There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.

> [!hint]- Hint(s)
> 1.  To view the level3.hash.bin file in the webshell, do: `$ bvi level3.hash.bin`
> 2. To exit `bvi` type `:q` and press enter.
> 3. The `str_xor` function does not need to be reverse engineered for this challenge.

---

### Step(s)
On line 44 there is a list called which contains 7 possibilities of the password. 
```python
["f7f3", "4aa2", "8e1d", "2266", "7243", "9f43", "f634"]
```
For this exercise  we can manually check each password since there is only 7 possibilities. 


### Flag
> [!question]- Flag
> picoCTF{m45h_fl1ng1ng_64840799}







