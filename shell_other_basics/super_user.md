# Super User

- The Super User, also known as `root user`, represents a user account in Linux with extensive powers, privileges, and capabilities.

- Root User has complete control over the system and can access any data stored on it, modify system configurations, change other user’s passwords, install software, and perform more administrative tasks in the shell environment.

- The usage of super user is critical to operating a Linux system properly and safely as it can potentially cause serious damage.

- To switch to super user use:

```bash
  su -
  sudo su
```

- To perform a command as a superuser as sudoers

```bash
 sudo <command>
```

**Note** that super user privileges should be handled with care due to their potential to disrupt the system’s functionality. Mistaken changes to key system files or unauthorized access can lead to severe issues.
