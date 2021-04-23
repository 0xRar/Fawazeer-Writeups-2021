- Challenge name: **`Memes`**
- Category: **`Network`**
- Difficulty: **`Easy`**
- Points: **`50`**

## Challenge Description:
> Our Memes website has been hacked!!
Can you help us and find out what they did?

https://fawazeer.net/files/memes.pcapng


## Solution: 
going fast throught the packets one by one with fast reading 
i found out that there is a file uploader or a Memes uploader ^_^

![image](https://user-images.githubusercontent.com/33517160/115821543-a97bf200-a40b-11eb-84bf-83aa7350d787.png)


so now we know that the hacker is exploiting an **`Unrestricted File Upload Vulnerability`** and than i
saw a POST Request for **`upload.php`** after reading the request we see that the hacker uploaded a **`shell.php`**
![image](https://user-images.githubusercontent.com/33517160/115822464-412e1000-a40d-11eb-80dd-69135e4d005d.png)


and now im looking for anything related to the **`shell.php`** 
![image](https://user-images.githubusercontent.com/33517160/115822828-df21da80-a40d-11eb-8719-aa0467f48046.png)

and after scorlling through the packets i saw an interesting request which is an upload for a JPEG Image,

i went to see what is this image: **`File -> Export Objects -> HTTP`**

![image](https://user-images.githubusercontent.com/33517160/115823134-7129e300-a40e-11eb-9e58-d2792846527f.png)

after clicking **`preview`** we get the flag:

![image](https://user-images.githubusercontent.com/33517160/115823204-94ed2900-a40e-11eb-8578-692146ba75b0.png)

Flag: **`flag{you_got_the_meme}`**
