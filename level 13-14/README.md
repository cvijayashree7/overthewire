# Bandit Level 13 → Level 14

## Objective

The private SSH key `sshkey.private` is available in the home directory of `bandit13`. We use this key to log in as `bandit14`.

## Step 1: Login as bandit13

```bash
ssh -p 2220 bandit13@bandit.labs.overthewire.org
```

Enter the Level 13 password.

## Step 2: Check the Private Key

```bash
ls -l sshkey.private
```

The file `sshkey.private` is available and readable by `bandit13`.

## Step 3: Exit to the Local Computer

The current server blocks SSH connections from localhost, so exit the Bandit server:

```bash
exit
```

This returns to the Windows PowerShell terminal.

## Step 4: Copy the Private Key

From the Windows terminal, copy the key to the local computer:

```powershell
scp -P 2220 bandit13@bandit.labs.overthewire.org:sshkey.private .\sshkey.private
```

Enter the `bandit13` password when prompted.

The file `sshkey.private` is now stored on the local computer.

## Step 5: Login as bandit14 Using the Key

```powershell
ssh -i .\sshkey.private -p 2220 bandit14@bandit.labs.overthewire.org
```

The private key is used for authentication, so a `bandit14` password is not required.

## Step 6: Find the Password

After successfully logging in as `bandit14`, run:

```bash
cat /etc/bandit_pass/bandit14
```

The command displays the password for the next level.

## Result

The password obtained is used to proceed from **Bandit Level 14 → Level 15**.

