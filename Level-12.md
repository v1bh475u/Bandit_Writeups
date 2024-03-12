The password is encoded in `ROT13`.<br>
![](./images/image-12.png)<br>
We will use `tr` command to shift characters by 13.<br>
Command: `cat data.txt| tr '[A-Za-z]' '[N-ZA-Mn-za-m]'`<br>
Password: `JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv`