# Linux User and Group Management Commands

This guide explains various Linux commands used to manage users and groups, such as creating users and groups, modifying user group memberships, and deleting groups.

## 1. Create a User

```bash
sudo useradd john
```

- **`useradd`**: Command to create a new user.
- **`john`**: The username of the new user being created.
- **`sudo`**: Runs the command with superuser privileges.

## 2. Create a Group

```bash
sudo groupadd developers
```

- **`groupadd`**: Command to create a new group.
- **`developers`**: The name of the group being created.

## 3. Add a User to a Group

```bash
sudo gpasswd --add john developers
```

OR

```bash
sudo gpasswd -a john developers
```

- **`gpasswd`**: Command to administer `/etc/group` and `/etc/gshadow`.
- **`--add` or `-a`**: Option to add a user to a group.
- **`john`**: The username being added to the group.
- **`developers`**: The group to which the user is being added.

## 4. Find a User's Groups

```bash
groups john
```

- **`groups`**: Command to display all groups a user is a member of.
- **`john`**: The username whose group memberships are being queried.

## 5. Remove a User from a Group

```bash
sudo gpasswd --delete john developers
```

OR

```bash
sudo gpasswd -d john developers
```

- **`--delete` or `-d`**: Option to remove a user from a group.
- **`john`**: The username being removed from the group.
- **`developers`**: The group from which the user is being removed.

## 6. Change a User's Primary Group

```bash
sudo usermod -g developers john
```

OR

```bash
sudo usermod --gid developers john
```

- **`usermod`**: Command to modify a user's account.
- **`-g` or `--gid`**: Option to change a user's primary group.
- **`developers`**: The new primary group.
- **`john`**: The username whose primary group is being changed.

## 7. Rename a Group

```bash
sudo groupmod --new-name programmers developers
```

OR

```bash
sudo groupmod -n programmers developers
```

- **`groupmod`**: Command to modify a group.
- **`--new-name` or `-n`**: Option to specify the new name for the group.
- **`programmers`**: The new name for the group.
- **`developers`**: The current name of the group being renamed.

## 8. Delete a Group

```bash
sudo groupdel programmers
```

- **`groupdel`**: Command to delete a group.
- **`programmers`**: The name of the group being deleted.

---

These commands provide basic user and group management functionalities in Linux, allowing you to create, modify, and delete users and groups as needed.
