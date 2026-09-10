 Level 15 → 16

Solution

First, connect to Level 15 using SSH.

`bash
ssh bandit15@bandit.labs.overthewire.org -p 2220
`

Then connect to the service running on port 30001 using SSL.

`bash
ncat --ssl localhost 30001
``

Enter the password of Level 15 when asked.
