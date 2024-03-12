We need to first find which port speaks ssl and also what it does.<br>
For this, we need to scan ports. We will use `nmap` command for this.<br>
command: `nmap -sV localhost -p 31000-32000`<br>
With the flag `sV`, we are specifying the target and `p` specifies the port.<br>
It takes a few minutes to scan and after that, we get following results.<br>
![](./images/image-17.png)<br>
There are 2 ports which speak ssl. However, one of them has echo as service which means it will just print whatever we input.<br>
Hence, we will connect to `31790` using netcat.<br>
command: `openssl s_client localhost:31790`<br>
We enter the password to get a private key.<br>
We copy that key and store it on our local machine.<br>
We then login as bandit17 and get the password from `/etc/bandit_pass/bandit17`.<br>
Password: `VwOSWtCA7lRKkTfbr2IDh6awj9RNZM5e`
