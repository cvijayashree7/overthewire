LEVEL 9 → LEVEL 10
Goal

Find the password among human-readable strings in data.txt.

Step 1
strings data.txt
Step 2

Look for the line containing several = characters.

A more convenient command is:

strings data.txt | grep "="
Step 3

The relevant output contains the password for bandit10.

What I learned

strings extracts readable text from binary/non-text data.

