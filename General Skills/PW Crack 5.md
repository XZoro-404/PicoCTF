---
tags:
  - python
  - password_cracking
---
# PW Crack 5
---
### Description
---
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/33/level5.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/33/level5.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/33/level5.hash.bin) in the same directory too. Here's a [dictionary](https://artifacts.picoctf.net/c/33/dictionary.txt) with all possible passwords based on the password conventions we've seen so far.
### Hints
---

> [!hint]- Hint(s)
> 1. Opening a file in Python is crucial to using the provided dictionary.
> 2. You may need to trim the whitespace from the dictionary word before hashing. Look up the Python string function, `strip`
> 3. The `str_xor` function does not need to be reverse engineered for this challenge.

### Step(s)
---
This is very similar to [[PW Crack 4]] the main difference being where the possible passwords are stored. The potential passwords are stored in their own file called `dictionary.txt`. We will once again be editing the password checker file (you can make this into a separate python script). First we need to bring in the dictionary file by adding the line 
```python
dict = open('dictionary.txt','r').readlines()
```
the 'r' puts the file in readmode and readlines will return every line as a new item in a list.
The function will be almost identical to the one in [[PW Crack 4]] with the exception of using `.strip()` to ensure there is no leading or trailing characters.

```python
def level_5_pw_check():
    for user_pw in dict:
        user_pw = user_pw.strip()
        user_pw_hash = hash_pw(user_pw)
        if(user_pw_hash == correct_pw_hash):
             print("Welcome back... your flag, user:")
             decryption = str_xor(flag_enc.decode(), user_pw)
             print(decryption)
             return
```

### Flag
---
> [!question]- Flag
> picoCTF{h45h_sl1ng1ng_36e992a6}







