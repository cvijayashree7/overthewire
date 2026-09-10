LEVEL 0 → LEVEL 1
Goal

Log in using SSH and find the password for Level 1 in a file called readme.

Step 1 — Connect
ssh bandit0@bandit.labs.overthewire.org -p 2220

When it asks for the password:

bandit0
Step 2 — List the files
ls

You should see:

readme
Step 3 — Read the file
cat readme

The output is the password for bandit1.

Step 4 — Login to Level 1
ssh bandit1@bandit.labs.overthewire.org -p 2220

Enter the password you got from readme.

What I learned
ssh → connects to a remote machine
ls → lists files
cat → displays file contents
