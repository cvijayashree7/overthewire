# Bandit Level 15 → Level 16

## Objective

The password for the next level is obtained by connecting to a service on **localhost port 30001** using **SSL/TLS encryption**.

## Step 1: Login as bandit15

```bash
ssh -p 2220 bandit15@bandit.labs.overthewire.org
```

Enter the password obtained from Level 14 → Level 15.

## Step 2: Connect to the SSL Service

```bash
openssl s_client -connect localhost:30001
```

The command establishes a secure TLS connection with the service.

A large amount of certificate and connection information may be displayed. This is normal.

## Step 3: Send the Password

When the connection is ready, paste the **bandit15 password** and press **Enter**.

For example:

```text
[Bandit 15 password]
```

If the password is correct, the service displays:

```text
Correct!
```

followed by the password for **Bandit Level 16**.

## Step 4: Save the Password

Copy the password displayed after:

```text
Correct!
```

This password is used to log in as `bandit16`.

## Result

The password obtained from the SSL service is the password required for **Bandi**
