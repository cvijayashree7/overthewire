LEVEL 12 → LEVEL 13

This is the multi-compression level.

Step 1

Create a temporary directory:

mkdir /tmp/bandit12
Step 2

Enter it:

cd /tmp/bandit12
Step 3

Copy the data:

cp ~/data.txt .
Step 4

Check the file:

file data.txt

You'll discover it is a hex dump.

Step 5

Convert the hex dump back to binary:

xxd -r data.txt data
Step 6

Check it:

file data

It will tell you what compression/archive format is next.

Then repeatedly:

mv data data.gz
gunzip data.gz

or, depending on what file says:

mv data data.bz2
bunzip2 data.bz2

or:

mv data data.tar
tar xf data.tar
Important

After every extraction, run:

file *

Then use the appropriate tool for the newly discovered format.

Eventually you'll reach a normal
