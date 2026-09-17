# Bandit Level 12 → Level 13

## Objective

The password for the next level is hidden inside a file called `data.txt`. The file has been repeatedly compressed using different compression formats.

## Step 1: Login to Bandit Level 12

```bash
ssh -p 2220 bandit12@bandit.labs.overthewire.org
```

Enter the Level 12 password when prompted.

## Step 2: Create a Temporary Directory

```bash
mktemp -d
```

Example output:

```text
/tmp/tmp.cYG51kFDZd
```

Change to the directory:

```bash
cd /tmp/tmp.cYG51kFDZd
```

## Step 3: Copy the File

```bash
cp ~/data.txt .
```

Check the file:

```bash
ls
```

Output:

```text
data.txt
```

## Step 4: Convert the Hex Dump

The file is a hexdump, so convert it back to binary format.

```bash
xxd -r data.txt data.bin
```

Check the file type:

```bash
file data.bin
```

It shows that the file is compressed.

## Step 5: Extract the Compressed File

The file may contain several layers of compression. Use `file` to identify the current format and extract it accordingly.

For gzip:

```bash
mv data.bin data.gz
gzip -d data.gz
```

For bzip2:

```bash
mv data data.bz2
bzip2 -d data.bz2
```

For gzip again:

```bash
mv data data.gz
gzip -d data.gz
```

For a tar archive:

```bash
tar -xf data
```

Continue checking the extracted file:

```bash
file ./*
```

The output identifies whether the next file is gzip, bzip2, or a tar archive.

## Step 6: Continue Until Plain Text Is Found

Repeat the appropriate extraction command based on the output of:

```bash
file ./*
```

The compression layers encountered include:

```text
gzip
bzip2
gzip
tar
tar
bzip2
...
```

Eventually, the final file becomes an ASCII text file.

## Step 7: Read the Password

Once `file` shows that the final file is ASCII text, display it:

```bash
cat <final-file>
```

The output is the password for **Bandit Level 13**.

## Result

The password obtained from Level 12 → Level 13 was:

```text
[Password obtained from the terminal]
```

This password is then used to log in as `bandit13`.
