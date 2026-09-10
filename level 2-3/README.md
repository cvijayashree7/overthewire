LEVEL 2 → LEVEL 3
Goal

The password is inside:

spaces in this filename
Step 1
ls
Step 2

Because the filename contains spaces, use quotes:

cat "spaces in this filename"

Alternative:

cat spaces\ in\ this\ filename
Step 3

The output is the password for bandit3.

Step 4
ssh bandit3@bandit.labs.overthewire.org -p 2220
What I learned

Quotes or \ can be used when filenames contain spaces.
