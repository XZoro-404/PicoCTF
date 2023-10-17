---
tags:
  - python
---
#### Description

Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/12/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/12/level1.flag.txt.enc) in the same directory too.

> [!hint]- Hint
>

---

### Step 1
After downloading the files on the webshell it is good to cat/nano each file.
from the flag file we can see some jumbled up text but from the python file we actually find something that seems useful
```python
### THIS FUNCTION WILL NOT HELP YOU FIND THE FLAG --LT ########################
def str_xor(secret, key):
    #extend key to secret length
    new_key = key
    i = 0
    while len(new_key) < len(secret):
        new_key = new_key + key[i]
        i = (i + 1) % len(key)        
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])
###############################################################################


flag_enc = open('level1.flag.txt.enc', 'rb').read()



def level_1_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    if( user_pw == "8713"):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")



level_1_pw_check()
```

### Step 2
We see that in the level_1__pw_check function that there is a if statement saying that if the `user_pw == "8713"` we will get the flag. 
After running the the python script and inputting the user password we get the flag



### Flag
> [!question]- Flag
> picoCTF{545h_r1ng1ng_1b2fd683}








