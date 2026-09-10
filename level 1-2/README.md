LEVEL 1 → LEVEL 2
Goal

The password is inside a file named -.

Step 1
ls

You will see:

-
Step 2

Don't use:

cat -

because - has special meaning to many Linux commands.

Use:

cat ./-
Step 3

The output is the password for bandit2.

Step 4
ssh bandit2@bandit.labs.overthewire.org -p 2220

Enter the password you just obtained.

What I learned

./- tells Linux that - is a filename in the current directory.

