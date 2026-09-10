LEVEL 10 → LEVEL 11
Goal

The password is stored in data.txt, but it is Base64 encoded.

Step 1
cat data.txt
Step 2

Decode it:

base64 -d data.txt
Step 3

The decoded output is the password for bandit11.

What I learned

Base64 is an encoding method, not encryption.
