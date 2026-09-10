# Level 3 → 4

## Solution

First, connect to Level 3 using SSH.

```bash
ssh bandit3@bandit.labs.overthewire.org -p 2220
```

The password is the one obtained from Level 2.

After logging in, list the files in the current directory.

```bash
ls
```

There is a directory named `inhere`.

Move into the directory.

```bash
cd inhere
```

List all files, including hidden files.

```bash
ls -la
```

A hidden file named `.hidden` is present.

Display its contents.

```bash
cat .hidden
```

The output is the password for Level 4.
