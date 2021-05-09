- Challenge name: **`Luqaimat`**
- Category: **`Forensics`**
- Difficulty: **`Medium`**
- Points: **`100`**

## Challenge Description:
> We received an encrypted zip file contains a photo
Can you help us to detect what is that photo?
And can you check if it's a regular photo or not?

https://fawazeer.net/files/luqaimat.zip

## Solution(UNCOMPLETE): 
So we have an encrypted zip file with jpeg inside it well there is 1 think we can think of here
which is using `john the ripper` to crack the zip file's password we are going to use 2 tools
from `john`


`zip2john`: zip2john will dump the password hash:
- `zip2john luqaimat.zip > hash.txt`

`john`: john will crack the password hash and give us the password
- `john hash.txt`

![image](https://user-images.githubusercontent.com/33517160/116229830-9e082e00-a75f-11eb-81b7-63c7a3c1fd0e.png)

`password: secret`

we know the password so we can get the jpeg now

and i couldn't solve it because of the jpeg i tried alot of tools to see if i
can catch something but no :( 
