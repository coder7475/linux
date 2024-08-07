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

- Shell provides a robust way of managing input and output streams of a program, this mechanism is known as redirection

- Linux is a multi-user and multi-tasking OS

- Every process in linux has 3 streams opened:

  - Standard Input (stdin) - This is where the process reads its - input from. The default is the keyboard.
  - Standard Output (stdout) - The process writes its output to stdout. By default, this means the terminal.
  - Standard Error (stderr) - The process writes error messages to stderr. This also goes to the terminal by default.

### Example

Store the output of a command into a file instead of printing it to the console, we can use the `>` operator:

```bash
  ls -al > file_list.txt
```

This command will write the output of `ls -al` into `file_list.txt`, whether or not the file initially existed. It will be created if necessary, and if it already exists – it will be overwritten.
