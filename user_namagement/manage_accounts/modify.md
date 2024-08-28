# Linux User Modification Commands

This guide provides explanations for various `usermod` and `chage` commands used to modify user attributes in Linux, such as changing the home directory, renaming users, changing shells, locking/unlocking accounts, setting account expiration, and managing password policies.

## 1. Change Home Directory

### Command

```bash
sudo usermod -d /home/otherdirectory -m john
```

### Explanation

- **`usermod`**: Command to modify a user's account properties.
- **`-d /home/otherdirectory`**: Specifies the new home directory for the user.
- **`-m`**: Moves the contents of the user's current home directory to the new home directory.
- **`john`**: The username whose home directory is being changed.

This command changes the home directory of the user `john` to `/home/otherdirectory` and moves all existing files to the new directory.

## 2. Change Username

### Command

```bash
sudo usermod --login jane john
```

OR

```bash
sudo usermod -l jane john
```

### Explanation

- **`--login` or `-l`**: Option to change the user's login name.
- **`jane`**: The new username.
- **`john`**: The current username.

This command changes the username from `john` to `jane`.

## 3. Change User Shell

### Command

```bash
sudo usermod --shell /bin/othershell jane
```

OR

```bash
sudo usermod -s /bin/othershell jane
```

### Explanation

- **`--shell` or `-s`**: Option to specify a new shell for the user.
- **`/bin/othershell`**: The new shell for the user.
- **`jane`**: The username for which the shell is being changed.

This command changes the default shell for the user `jane` to `/bin/othershell`.

## 4. Disable User Account

### Command

```bash
sudo usermod --lock jane
```

OR

```bash
sudo usermod -L jane
```

### Explanation

- **`--lock` or `-L`**: Option to lock a user account.
- **`jane`**: The username whose account is being locked.

This command locks the user `jane`'s account, preventing them from logging in.

## 5. Enable User Account

### Command

```bash
sudo usermod --unlock jane
```

OR

```bash
sudo usermod -U jane
```

### Explanation

- **`--unlock` or `-U`**: Option to unlock a user account.
- **`jane`**: The username whose account is being unlocked.

This command unlocks the user `jane`'s account, allowing them to log in again.

## 6. Set Account Expiration Date

### Command

```bash
sudo usermod --expiredate 2024-12-10 jane
```

OR

```bash
sudo usermod -e 2024-12-10 jane
```

### Explanation

- **`--expiredate` or `-e`**: Option to set the expiration date for the user account.
- **`2024-12-10`**: The date on which the account will expire.
- **`jane`**: The username for which the expiration date is being set.

This command sets the expiration date of the user `jane`'s account to December 10, 2024.

### Remove Account Expiration Date

```bash
sudo usermod -e "" jane
```

- **`-e ""`**: Sets the expiration date to an empty string, removing any expiration date for the user `jane`.

## 7. Manage Password Expiration

### Command to Expire Password Immediately

```bash
sudo chage --lastday 0 jane
```

OR

```bash
sudo chage -d 0 jane
```

### Explanation

- **`chage`**: Command to change user password expiration information.
- **`--lastday` or `-d`**: Sets the date of the last password change.
- **`0`**: Sets the last password change date to "0," forcing the user `jane` to change their password on the next login.

### Undo Password Expiration

```bash
sudo chage -d -1 jane
```

- **`-d -1`**: Resets the last password change date, effectively undoing the forced password change requirement.

### Set Maximum Days Between Password Changes

```bash
sudo chage --maxdays 30 jane
```

OR

```bash
sudo chage -M 30 jane
```

### Explanation

- **`--maxdays` or `-M`**: Option to set the maximum number of days before a password must be changed.
- **`30`**: Sets the maximum days to 30.
- **`jane`**: The username for which the maximum days between password changes are being set.

This command forces the user `jane` to change their password every 30 days.

## 8. Find Password Policy Information

### Command

```bash
sudo chage --list jane
```

OR

```bash
sudo chage -l jane
```

### Explanation

- **`--list` or `-l`**: Option to display the password expiration information for a user.
- **`jane`**: The username for which the information is being displayed.

This command lists all password expiration details for the user `jane`, including the last password change date, expiration date, and maximum password age.

---

These commands provide essential tools for managing user accounts and their security policies in Linux environments.
