LEVEL 8 → LEVEL 9
Goal

Find the line in data.txt that occurs only once.

Step 1
sort data.txt

But we need the unique line.

Step 2

Use:

sort data.txt | uniq -u
Step 3

The output is the password for bandit9.

What I learned
sort sorts lines
uniq -u displays lines occurring only once
| sends one command's output into another command
