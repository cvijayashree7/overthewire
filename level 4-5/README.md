LEVEL 4 → LEVEL 5
Goal

Inside inhere are several files. The password is in the only human-readable file.

Step 1
ls
Step 2
cd inhere
Step 3

List the files:

ls

You'll see several files such as:

-file00
-file01
-file02
...
Step 4

Check their file types:

file ./*

Look through the output for:

ASCII text

or another human-readable text file.

Step 5

Read that file:

cat ./FILENAME

Replace FILENAME with the file identified by file.

Step 6

The output is the password for bandit5.

What I learned

file tells you what type of data a file contains.

