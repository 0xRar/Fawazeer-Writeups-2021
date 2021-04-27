- Challenge name: **`Authentication system`**
- Category: **`Reverse`**
- Difficulty: **`Normal`**
- Points: **`50`**

## Challenge Description:
> Negan made a secure authentication system for us
Can you check if you can break this system?

## Solution:
its easy to find the flag in this challenge but
i kinda overthinked it, first thing i tried is:

`strings authentication` but i didint look closely so i didin't find it but if you look you
can actually see the flag leaked in the strings.

`strings authentication`
```
flagf
easy
_peasy_
lemof
squeezy
```
**`flag{easy_peasy_lemon_squeezy}`**

and thats the reason why i didint find it using `strings`
because it doesn't look like a flag

and the other way is using `radare2`:

```
r2 -d authentication
aaa
pdf @main
```
- pdf == Print disassembly of function
- r2 -d == it will run radare2 in debug mode
- aaa == analyze the binary and functions

we will find the flag in the output:
```
0x564611820205      c700666c6167   mov dword [rax], 0x67616c66 ; 'flag'
0x56461182020b      66c740047b00   mov word [rax + 4], 0x7b ; '{'
0x56461182023a      c70065617379   mov dword [rax], 0x79736165 ; 'easy'
0x56461182026d      48be5f706561.  movabs rsi, 0x5f79736165705f ; '_peasy_'
0x5646118202a3      c7006c656d6f   mov dword [rax], 0x6f6d656c ; 'lemo'
0x5646118202a9      66c740046e5f   mov word [rax + 4], 0x5f6e ; 'n_'
0x5646118202dc      48be73717565.  movabs rsi, 0x797a6565757173 ; 'squeezy'
0x564611820312      66c7007d00     mov word [rax], 0x7d    ; '}'
```

Flag: **`flag{easy_peasy_lemon_squeezy`**
