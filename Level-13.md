We are given hexdump of a file compressed many times.<br>
We make a temporary directory using `mktemp -d` and using `cp ~/data.txt .`.<br>
First, we reverse hexdump using command `mv data.txt dump` and then `xxd -r dump compress`.<br>
We see that starting bytes of file are `1f8b`. This is the signature of gzip compressed files.<br>
![](./images/image-13.1.png)<br>
We rename the file using `mv compress data.gz` and then decompress it using `gzip -d data.gz`.<br>
We use `xxd data` to see the file type. The starting bytes are `425a`.<br>
![](./images/image-13.2.png)<br>
This is signature of `bzip2` compression. <br>
Again the magic bytes are `1f8b`. Hence, we repeat the procdure and get something weird. It doesn't seem to have any magic bytes.<br>
![](./images/image-13.3.png) <br>
But we can see the `data5.bin`. Thus, it seems that we have an archive now. Hence, we use `tar`.<br>
Command: `tar -xf data.tar`<br>
![](./images/image-13.4.png)<br>
We again seem to have an archive.<br>
We again go thorught the same process and get `425a` as starting bytes of `data6.bin`. It is bzip2 compression. <br>
Now, we again get an archive. We retrieve `data8.bin`.<br>
This file is just a simple ascii file. We simply use `cat` to read the file.<br>
Password: `wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw`