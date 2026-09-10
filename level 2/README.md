# Level 2 → 3

## Solution

First, connect to Level 2 using SSH.

```bash
ssh bandit2@bandit.labs.overthewire.org -p 2220
```

The password is the one obtained from Level 1.

List the files in the current directory.

```bash
ls
```

There is a file named `spaces in this filename`.

Since the filename contains spaces, put the filename inside quotes.

```bash
cat "spaces in this filename"
```

The output is the password for Level 3.
