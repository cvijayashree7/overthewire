Level 14→Level 15
The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost.

According to the hint we have to connect to port 30000 on localhost and we have to send a string containing the current password.

To do this I ran “nc localhost 30000”.

The username for level 14 is bandit14, and a connection should be made to the server at localhost.

No password will be requested when connecting with the private key. Once level 14 is logged into, 

the password for the current level can be found in a file named bandit14. This file is located in the /etc/bandit_pass/bandit14 directory, as indicated in the login banner.

cat /etc/bandit_pass/bandit14 | nc localhost 30000

