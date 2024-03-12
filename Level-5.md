We login to see multiple files inside a directory.<br>
Now, we know that there's only 1 file that is human readable.<br>
For human-readable, we can use `strings` command along with wildchar `*` to get the password.<br>
Command: `strings inhere/file-0*`<br>
This command will print all sequences of readable lines from all files starting with `file-0`.<br>
![strings](./images/image-2.png)<br>
Password: `lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR`<br>