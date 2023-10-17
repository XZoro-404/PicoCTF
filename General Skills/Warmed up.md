---
tags:
  - hexadecimal
  - base10
  - conversion
---
#### Description

What is 0x3D (base 16) in decimal (base 10)?

---
> [!question]- Hint
>Submit your answer in our flag format. For example, if your answer was '22', you would submit 'picoCTF{22}' as the flag.

### Step 1
Converting from hexadecimal (base16) to base10 

In hexadecimal the letters equals the following 
A = 10, B = 11, C = 12, D = 13, E = 14, F = 15
and to convert from hex to base10 you just multiply every number position by 16 to its index where 0 index is in the ones place. so to convert we can do the following
3 * 16$^1$ + 13 * 16$^0$ = 61

> [!question]- Flag
> picoCTF{61}


