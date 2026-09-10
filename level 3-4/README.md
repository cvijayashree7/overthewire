LEVEL 3 → LEVEL 4
Goal

The password is inside a hidden file in the inhere directory.

Step 1
ls

You should see:

inhere
Step 2

Enter it:

cd inhere
Step 3

Normal ls may show nothing.

Use:

ls -a

You should see:

.hidden
Step 4

Read it:

cat .hidden
Step 5

Use that output as the password for bandit4.

ssh bandit4@bandit.labs.overthewire.org -p 2220
What I learned

ls -a shows hidden files.


