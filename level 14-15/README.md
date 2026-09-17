# Bandit Level 14 → Level 15

## Objective

The password for the current level must be sent to a service running on **localhost port 30000**.

## Step 1: Login as bandit14

```bash
ssh -p 2220 bandit14@bandit.labs.overthewire.org
```

Enter the password obtained from Level 13 → Level 14.

## Step 2: Read the Current Password

```bash
cat /etc/bandit_pass/bandit14
```

Copy the password displayed by the command.

## Step 3: Connect to Port 30000

```bash
nc localhost 30000
```

The service waits for input.

## Step 4: Send the Password

Paste the password obtained in Step 2 and press **Enter**.

If the password is correct, the service returns the password for **Bandit Level 15**.

## Result

The password obtained from the service is used to log in to **bandit15**.

```text
[Password obtained from the terminal]
```
