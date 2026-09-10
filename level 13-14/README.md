</>Step 1: Log back into Bandit 13

Open your personal terminal and log into Level 13 using the password you already have:

bashssh bandit13@bandit.labs.overthewire.org -p 2220

Use code with caution.

Step 2: Fix the "Host Verification"
TrapWhen you try to connect to the next level, the server will almost always ask you this exact question:

text:

Are you sure you want to continue connecting (yes/no/[fingerprint])? yes 

you should give



Step 3: Run the proper connection commandOnce you are inside bandit13,

run this exact command (using 127.0.0.1 instead of localhost to avoid any network routing bugs):

bashssh -i sshkey.private bandit14@127.0.0.1 -p 2220
