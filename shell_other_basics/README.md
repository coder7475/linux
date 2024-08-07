# Shell Basics

## Command Path in Shell Basics

- Linux commands are nothing but programs residing in particular directories

- Commands need absolute path to run commands

- Shell automatically search the directories in correct order

- This path is stored in `$PATH` variable

### Command to Find all Directories

```bash
  echo $PATH
```

## Environment Variables(ENV) Under Shell Basics

- ENV are dynamic named values that can affect the behavior of running process in a shell.

- ENV includes user's home directory, command search path, terminal type, program preferences etc.

- ENV help to contribute to the fantastic and customizable flexibility you see in Unix systems.

- They provide a simple way to share configuration settings between multiple applications and processes in Linux

**List all Environments Variable**:

```bash
env
```

**Remember**, every shell, such as **Bourne shell**, **C shell**, or **Korn shell** in Unix or Linux has different syntax and semantics to define and use environment variables.

## Redirects
