- Challenge name: **`Recursion`**
- Category: **`Programming`**
- Difficulty: **`Normal`**
- Points: **`50`**

## Challenge Description:
> Recursion recursion recursion recursion recursion
recursion recursion recursion recursion recursion
recursion recursion recursion recursion ...


## Solution: 

script By [codaholikid](https://twitter.com/codaholikid):
```
#!/usr/bin/env bash
# @author: codaholikid

unzip recursion.zip
for i in {554..0}; do
    unzip recursion$i.zip
    rm recursion$i.zip
cat flag.txt
done
```

What it's doing is it's going to unzip the original zipfile. Then you notice the unzipped file has a number attached to it. The script will iterate from number 554 to 0....with the last zipfile being recursion0.zip that has the flag, and when it unzips that file, you'll get the flag.

![image](https://user-images.githubusercontent.com/33517160/116865636-a86c7100-ac12-11eb-89e6-16670ed1b23a.png)


Flag: **`flag{zip_into_zip_into_zip_etc}`**
