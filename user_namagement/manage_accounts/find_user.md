# Linux Commands to Find User Information

This guide explains the Linux commands to find user-related information, such as the user ID (UID) and the currently logged-in user's name.

## 1. Find User ID

### Command

```bash
id
```

### Explanation

The `id` command is used to display user identity information in Linux. When executed, it shows the following details:

- **User ID (UID)**: The numeric identifier associated with the user.
- **Group ID (GID)**: The numeric identifier associated with the user's primary group.
- **Groups**: A list of all groups the user is a member of, including the primary group.

#### Example Output

```bash
uid=1000(username) gid=1000(username) groups=1000(username),4(adm),27(sudo)
```

- **`uid=1000(username)`**: Displays the user ID (UID) and the corresponding username.
- **`gid=1000(username)`**: Displays the group ID (GID) and the corresponding group name for the user's primary group.
- **`groups=1000(username),4(adm),27(sudo)`**: Lists all groups the user belongs to, along with their numeric IDs and names.

The `id` command provides a comprehensive overview of a user's identity, making it useful for checking user permissions and group memberships.

## 2. Find User Name

### Command

```bash
whoami
```

### Explanation

The `whoami` command is used to display the username of the current user. It prints the effective user name associated with the current user session.

- **`whoami`**: Literally stands for "who am I," and outputs the current user's username.

#### Example Output

```bash
username
```

- **`username`**: Displays the username of the currently logged-in user.

The `whoami` command is straightforward and provides a quick way to verify the current user's identity, especially useful in scripts or when managing multiple user sessions.

---

These commands are helpful for identifying user information and managing user accounts in Linux environments.
