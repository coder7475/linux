# Linux User Management Commands and Options

This guide provides explanations of various Linux commands related to managing users, including creating, modifying, and deleting users, as well as setting user-specific options.

## 1. Create a New User

```bash
sudo useradd john
```

### Result:

1. **New user**: `john` is created.
2. **New group**: A group named `john` is also created.
3. **New directory**: A home directory at `/home/john` is created.
4. **New user shell**: The default shell is set to `/bin/bash`.
5. **Home directory files**: All files from `/etc/skel` (the skeleton directory) are copied to `/home/john`.

## 2. Find Default Settings for New Users

```bash
useradd --defaults
```

- **`useradd --defaults`**: Displays the default settings used when creating a new user.

To find more explanations of these default settings:

```bash
cat /etc/login.defs
```

- **`cat /etc/login.defs`**: Displays the content of the `/etc/login.defs` file, which contains default configuration settings for user creation, such as password expiration, UID ranges, etc.

## 3. Set Up a Password for a User

```bash
sudo passwd john
```

- **`passwd`**: Command to set or change the password for a user.
- **`john`**: The username for which the password is being set.

## 4. Delete a User Account

```bash
sudo userdel john
```

- **`userdel`**: Command to delete a user account.
- **`john`**: The username of the account being deleted.

## 5. Delete a User and Their Home Directory

```bash
sudo userdel --remove john
```

- **`--remove`**: Option to remove the user's home directory and mail spool in addition to deleting the user account.
- **`john`**: The username of the account being deleted.

## 6. Use a Different Shell for a User

```bash
sudo useradd --shell /bin/othershell --home-dir /home/otherdirectory/ john
```

OR

```bash
sudo useradd -s /bin/othershell -d /home/otherdirectory/ john
```

OR

```bash
sudo useradd -s /bin/othershell john
```

- **`--shell` or `-s`**: Option to specify a different shell (e.g., `/bin/othershell`) for the user.
- **`--home-dir` or `-d`**: Option to specify a different home directory (e.g., `/home/otherdirectory/`).
- **`john`**: The username being created or modified.

## 7. Find User Data

```bash
cat /etc/passwd
```

- **`cat /etc/passwd`**: Displays the contents of the `/etc/passwd` file, which contains user account information such as username, user ID (UID), group ID (GID), home directory, and shell.

## 8. Create a User with a Custom UID

```bash
sudo useradd --uid 1100 smith
```

- **`--uid`**: Option to specify a custom user ID (UID) for the new user.
- **`1100`**: The custom UID being assigned.
- **`smith`**: The username being created with the specified UID.

## 9. Check Home Directory Permissions

```bash
ls -l /home/
```

- **`ls -l`**: Command to list files and directories with detailed information, including permissions.
- **`/home/`**: Directory where user home directories are located.

To view permissions with user IDs (UIDs):

```bash
ls -ln /home
```

- **`-n`**: Option to display numeric user and group IDs instead of names.

---

These commands provide a comprehensive overview of user management in Linux, including creating, modifying, and deleting users, setting custom user options, and checking default and custom user settings.
