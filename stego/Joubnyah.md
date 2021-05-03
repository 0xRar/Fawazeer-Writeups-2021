- Challenge name: **`Joubnyah`**
- Category: **`Steganography`**
- Difficulty: **`Easy`**
- Points: **`25`**

## Challenge Description:
> In conclusion, we offer you this little dessert
We hope you have fun with our challenges
Good bye lovely guys, we will miss you <3

https://fawazeer.net/files/joubnyah.zip


## Solution:
A very straight forward challenge idk why im doing a writeup for it, 

so we get this zip file `unzip Joubnyah.zip`,than i triad exiftool on the challenge but nothing there
so i tried strings maybe the flag is there 

`strings joubnyah.jpg | grep "flag"` and yes we get the flag

Flag: **`flag{yummy_true?}`**
