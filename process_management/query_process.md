# Query Running Processes - BASH SHELL

Output shows all the process associated with the current user & terminal session

```bash
  ps
```

# More Complete picture

Show all process owned by all users

```bash
  ps aux
```

# Pipeline to find specific process

Syntax:

```bash
ps aux | grep process_name
```

Example:

```bash
ps aux | grep bash
```

Similar command:

```bash
  ps -ef | grep process_name
```

Example:

```bash
  ps -ef | grep nginx
```

# Get Process ID (PID) of a process

```bash
pgrep bash
```

# Grab the first process spawned at boot called init

```bash
pgrep init
```

**PPID**: A process's parent is the process that was responsible for spawning it.
Parent process has a PPID.
