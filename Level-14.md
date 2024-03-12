When we login, we see that there's an ssh-private on the server.<br>
![](./images/image-14.1.png)<br>
It is said that we won't get password for the next level but a private key.<br>
Here, the challenge wants to teahc us that using password is not the only way to login to a server. We can also use sshkeys to do the same.<br>
![](./images/)<br>
We first use command `scp -P 2220 bandit13@bandit.labs.overthewire.org:~/sshkey.private .`<br>
![](./images/image-14.2.png)<br>
Now, to login to next level, we will use `ssh -i ./sshkey.private bandit13@bandit.labs.overthewire.org -p 2220`.<br>
Then we can read the password of `bandit14` present inside `/etc/bandit_pass/bandit14`.<br>
Password: `fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq`