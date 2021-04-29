- Challenge name: **`Psycho`**
- Category: **`Network`**
- Difficulty: **`Normal`**
- Points: **`50`**

## Challenge Description:
> We captured some packets from the network
And we think there is a psycho attacker between us
Can you find out what they are trying to send?

https://fawazeer.net/files/psycho.pcapng

## Solution: 
this one is easy but it could be kinda hard for some beginners, not much going in these packets
but as i was reading the packets i flaged something

![image](https://user-images.githubusercontent.com/33517160/116535964-12bca300-a8ed-11eb-8cc1-65757f9c6775.png)

what we see here is an svg

SVG stands for Scalable Vector Graphics. SVG is used to define vector-based graphics<br>
for the Web. SVG defines the graphics in XML format. Every element and every attribute<br>
in SVG files can be animated. SVG is a W3C recommendation.<br>



lets copy as pintable text & delete the extra bytes

### svg:
```
<?xml version="1.0" encoding="UTF-8"?>
<svg xmlns="http://www.w3.org/2000/svg" height="296" width="296" class="pyqrcode"><path transform="scale(8)" stroke="#000" class="pyqrline" d="M4 4.5h7m1 0h2m1 0h1m10 0h7m-29 1h1m5 0h1m1 0h1m1 0h1m1 0h1m1 0h2m1 0h2m1 0h1m1 0h1m5 0h1m-29 1h1m1 0h3m1 0h1m1 0h1m2 0h1m2 0h1m1 0h1m1 0h1m3 0h1m1 0h3m1 0h1m-29 1h1m1 0h3m1 0h1m2 0h1m2 0h1m1 0h3m3 0h1m1 0h1m1 0h3m1 0h1m-29 1h1m1 0h3m1 0h1m2 0h3m2 0h4m1 0h2m1 0h1m1 0h3m1 0h1m-29 1h1m5 0h1m1 0h2m1 0h1m2 0h4m2 0h1m1 0h1m5 0h1m-29 1h7m1 0h1m1 0h1m1 0h1m1 0h1m1 0h1m1 0h1m1 0h1m1 0h7m-21 1h2m1 0h3m1 0h1m1 0h2m-17 1h3m1 0h1m1 0h7m1 0h1m4 0h3m2 0h3m-29 1h1m9 0h1m1 0h1m1 0h1m2 0h2m1 0h1m1 0h7m-29 1h5m1 0h1m3 0h3m1 0h6m2 0h2m2 0h1m-27 1h1m1 0h1m2 0h1m1 0h1m3 0h2m1 0h1m1 0h1m1 0h3m1 0h1m1 0h2m1 0h2m-27 1h7m1 0h4m4 0h3m4 0h1m-23 1h2m2 0h1m1 0h1m3 0h1m3 0h4m1 0h7m-29 1h1m3 0h11m5 0h1m2 0h1m-24 1h4m3 0h2m1 0h1m1 0h1m2 0h1m2 0h5m2 0h1m-25 1h2m3 0h1m1 0h3m1 0h2m1 0h1m1 0h1m1 0h1m3 0h1m2 0h3m-29 1h2m3 0h1m2 0h1m1 0h2m1 0h4m4 0h8m-29 1h1m3 0h1m1 0h2m2 0h2m8 0h2m1 0h1m1 0h2m-27 1h1m1 0h1m2 0h1m3 0h1m2 0h1m1 0h1m1 0h2m2 0h2m1 0h1m1 0h1m-26 1h1m5 0h4m6 0h1m1 0h7m1 0h1m-19 1h1m2 0h1m1 0h1m1 0h2m2 0h2m3 0h1m2 0h2m-29 1h7m3 0h1m2 0h1m1 0h2m1 0h1m1 0h1m1 0h1m1 0h2m-26 1h1m5 0h1m2 0h2m2 0h1m1 0h1m1 0h1m1 0h2m3 0h2m2 0h1m-29 1h1m1 0h3m1 0h1m1 0h1m1 0h1m1 0h1m1 0h1m1 0h3m1 0h5m1 0h1m1 0h1m-29 1h1m1 0h3m1 0h1m1 0h2m1 0h5m1 0h4m2 0h1m-24 1h1m1 0h3m1 0h1m1 0h1m1 0h3m1 0h2m1 0h2m3 0h4m1 0h1m-28 1h1m5 0h1m2 0h1m2 0h2m2 0h1m1 0h3m2 0h1m1 0h1m1 0h1m-28 1h7m3 0h1m2 0h1m1 0h1m3 0h1m2 0h4"/></svg>

```
now we need to put this svg code into a file and save as **`filename.svg`**
after that open the svg in a browser now we see the image or the qr code

![image](https://user-images.githubusercontent.com/33517160/116537431-e43fc780-a8ee-11eb-9ac7-82c2abe60a33.png)

after reading the qr code we get the flag:

![image](https://user-images.githubusercontent.com/33517160/116538439-32a19600-a8f0-11eb-974a-20f09d2bb5cd.png)

Flag: **`flag{ops_qr_in_a_svg}`**
