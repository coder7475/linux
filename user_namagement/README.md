# User Management

- Efficient user management is crucial for maintaining a secure and well-organized Linux environment

## What are Users in Linux?

- Users refer to individuals or entities that interact with the operating system by logging in and performing various tasks

- A user in Linux is associated with a **user account**, which consists of several properties defining their **identity** and **privileges** within the system. These properties are a _username_, _UID_ (User ID), _GID_ (Group ID), _home directory_, _default shell_, and _password_.

## Types of Users in Linux

1. **System Users**: Created by system during installation and are used to run _system services_ and _applications_.

2. **Regular Users**: Created by the administrator and can access the system and its resources based on _permissions_.

### Example

Let's meet CTechCo's diverse workforce, consisting of individuals who interact with the Linux system through user accounts. Meet John, a developer; Lisa, a system administrator; and Sarah, a marketing manager. They each have unique usernames such as "johndoe," "lisasmith," and "sarahsmith," respectively. These usernames act as their identification within the Linux system.

## How to create users

- Syntax:

```bash
  sudo useradd -u UID -d Home_Directory -s Default_Shell User_Name
```

- Example

```bash
 sudo useradd -u 1002 -d /home/john -s /bin/bash john
```

This command creates John's account with uid (-u) as 1002, the home directory (-d) as /home/john and sets (-s) /bin/bash as his default shell.

- Verify new user

```bash
  id john
```

- Find all users of linux

```bash
  cat /etc/passwd
```

- Format of user shown:

```bash
  john:x:1002:1002::/home/john:/bin/bash
```

Heres what above format represents:

- `john`: User Name
- `x`: encrypted password of the user
- `1002`: This is UID (User ID)
- `1002`: This is GID (Group ID)
- `/home/john`: home directory of the user
- `/bin/bash`: default shell of the user

## How to delete a user

- Syntax:

```bash
  sudo userdel username
```

- Example

```bash
  sudo userdel john
```

This will delete the user account for `john`, along with their home directory and any files or directories owned by the user.

### References

- https://www.freecodecamp.org/news/how-to-manage-users-in-linux/
