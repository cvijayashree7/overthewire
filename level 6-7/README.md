LEVEL 6 → LEVEL 7
Goal

Find a file somewhere on the server that:

is owned by user bandit7
is owned by group bandit6
is 33 bytes
Step 1

From the home directory:

cd ~
Step 2

Run:

find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
Step 3

You should get the location of the correct file.

Step 4

Read it:

cat /path/to/file
Step 5

The output is the password for bandit7.

What I learned

find can search the entire filesystem using ownership and size.



millionth
Step 1
