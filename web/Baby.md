- Challenge name: **`Baby`**
- Category: **`Web`**
- Difficulty: **`Easy`**
- Points: **`25`**

## Challenge Description:
> It's a baby web challenge
Can you get the flag?


## Solution: 
we get a web page with nothing on the source code other than a `<pre>` with ascii art

```
<pre class="">            .-"''-.  _
          .'       `( \ 
        @/            ')   ,--,__,-"
        /        /      \ /     /   _/
      __|           ,   |/         /
    .~  `\   / \ ,  |   /
  .~      `\    `  /  _/   _/
.~          `\  ~~`__/    /
~             `--'/
             /   /    /
            /  /'    /     Baby shark do do do do 
</pre>
```

i decided to check burpsuite but before that i wanted to check if there is a `robots.txt`
and yes we get 1 disallowed html page

```
User-agent: *
Disallow: /babyflag.html
```

in the `babyflag.html` page you can't see the flag normally because it has a `<font color=white>`
good one hitman,
i used `ctrl a` and i saw the flag without opening the source code but, you need to open
source code for every challenge so you know what's going on. 

```
   ,=""=,
    c , _,{
    /\  @ )                 __
   /  ^~~^\          <=.,__/ '}=
  (_/ ,, ,,)          \_ _>_/~
   ~\_(/-\)'-,_,_,_,-'(_)-(_)  
   
                 flag{you_got_dat_baby_flag}
  
```

Flag: **`flag{you_got_dat_baby_flag}`**
