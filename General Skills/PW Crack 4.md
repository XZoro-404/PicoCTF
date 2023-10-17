---
tags:
  - python
  - password_cracking
---
# PW Crack 4
---
### Description
---
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/20/level4.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/20/level4.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/20/level4.hash.bin) in the same directory too.There are 100 potential passwords with only 1 being correct. You can find these by examining the password checker script.
### Hints
---

> [!hint]- Hint(s)
> 1. A for loop can help you do many things very quickly.
> 2. The `str_xor` function does not need to be reverse engineered for this challenge.

### Step(s)
---
When looking at the password checker we have a list of 100 possible passwords on line 45. Since this would take a significant time to do manually we can utilize a for loop in python. We could do this all in a separate file to find the password but I would prefer to show you how to do it within the file itself. (If you wish you can create a separate file using the same method I am using here). Change the function `level_4_pw_check` to resemble the following. (To do this on the command line you can use Nano, Vim, or whichever editor you prefer)
```python
def level_4_pw_check():
    pos_pw_list = ["158f", "1655", "d21e", "4966", "ed69", "1010", "dded", "844c", "40ab", "a948", "156c", >

    for x in pos_pw_list:
        user_pw_hash = hash_pw(x)
        if( user_pw_hash == correct_pw_hash ):
            decryption = str_xor(flag_enc.decode(), x)
            print("Welcome back... your flag, user:")
            print(decryption)
            return
```
After changing the code in the password checker make sure to save and run it which will give you the flag.
### Flag
---
> [!question]- Flag
> picoCTF{fl45h_5pr1ng1ng_d770d48c}








