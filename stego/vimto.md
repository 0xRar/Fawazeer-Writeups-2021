- Challenge name: **`Vimto`**
- Category: **`Steganography`**
- Difficulty: **`Easy`**
- Points: **`25`**

## Challenge Description:
> Hey hacker, are you thirsty?
Then try our special Vimto drink
It has a lot of secret flavors 


## Solution: 
we get a zip file `unzip vimto.zip`

than we have a png file i tried strings but i got nothing & because its a png i tried binwalk
to see if there is anything and nope nothing in there 

there is a tool im missing here, what about meta data? maybe there is something there so i tried `exiftool`....

**`exiftool vimto.png`**

![image](https://user-images.githubusercontent.com/33517160/116862850-0ba7d480-ac0e-11eb-8dc7-8b88367f1729.png)


Flag: **`flag{this_is_da_best_drink_ever}`**
