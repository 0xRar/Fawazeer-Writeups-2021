- Challenge name: **`Control Center`**
- Category: **`Web`**
- Difficulty: **`Easy`**
- Points: **`50`**

## Challenge Description:
> We have a system called Fawazeer Control Center
It's a secure system and works internally only
Can you check if it's really secure or not?


## Solution: 
This one is easy if you did it before.

![image](https://user-images.githubusercontent.com/33517160/115729975-8d863b00-a38e-11eb-90d1-a6a225d3be71.png)

**There is 2 kind of these challenges, there is one where they tell you you need to come from
this DNS example: `google.com` and you need to Intercept the HTTP Request with `BurpSuite` and modify the
referrer to `google.com` to get the flag,**

**but this web app is hosted locally and can be
accessed only from `127.0.0.1` or `localhost`
so `X-Forwarded-For` header will be the solution here**

## Steps:
- Intercept the HTTP Request

![image](https://user-images.githubusercontent.com/33517160/115741072-16ee3b00-a398-11eb-8f22-d2c29946d703.png)

- (`CTRL + R`) send to repeater
- add `X-Forwarded-For: 127.0.0.1` to the HTTP Request Header

the Request should look like this:

![image](https://user-images.githubusercontent.com/33517160/115741605-94b24680-a398-11eb-9cb1-4f03b1a62232.png)

![image](https://user-images.githubusercontent.com/33517160/115741876-cfb47a00-a398-11eb-8c0c-6a1fec44c23d.png)

Flag: **`flag{to_spoof_or_not_to_spoof}`**
