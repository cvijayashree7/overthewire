# Level 12 → 13

## Goal

The file `data.txt` contains a hexdump of a repeatedly compressed file. The task is to decompress it until the password is obtained.

## Step : Create a temporary directory

```bash
mkdir /tmp/b12
cp data.txt /tmp/b12
cd /tmp/b12
xxd -r data.txt data
mv data data.gz
gunzip data.gz
cat data
## CONCLUSION
PUT SSH command and get password
