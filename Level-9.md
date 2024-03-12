In this level, password is written only once while others are repeated. <br>
Hence, we will use `uniq -u` command which will print only unique lines.<br>
But for it to work, we need to have sorted lines. Hence, we will use `sort` first and then `uniq`.<br>
Command: `sort data.txt| uniq u`<br>
![](./images/image-9.png)<br>
Password:`EN632PlfYiZbn3PhVK3XOGSlNInNE00t`