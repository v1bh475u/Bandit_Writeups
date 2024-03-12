Here, the `.bashsrc` had code which was logging us out as soon as we logged in.<br>
Luckily, we don't need to stay on the server for running commands. We can simply run commands from `ssh`. ssh will execute whatever command we concatenate after the login command.<br>
Command:`ssh bandit18@bandit.labs.overthewire.org -p 2220 cat readme`<br>
Password:`awhqfNnAbc1naukrpqDYcF95h7HoMTrC`