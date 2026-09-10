LEVEL 11 → LEVEL 12
Goal

The password is encrypted using ROT13.

Step 1
cat data.txt
Step 2

Use tr:

cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
Step 3

The output is the password for bandit12.

What I learned

ROT13 replaces each letter with the letter 13 positions away.
