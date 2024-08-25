# Text Processing

Linux, being a robust operating system, provides powerful tools for text searching, manipulation, and processing.

Users can utilize commands like `awk`, `sed`, `grep` and `cut` for text filtering, substitution and handling regular expression.

## Stdout and stderr

- This concept is fundamental in linux text processing.

- When a program is executed in linux three processing channels opened:

  - STDIN (Standard Input)
  - STDOUT (Standard Output): channel used to send shell commands
  - STERR (Standard output): channel for sending error message

- Example

```bash
    command > stdout.txt 2>stderr.txt
```

In this example, the ”>” operator redirects the standard output (stdout) into a text file named stdout.txt, while “2>” redirects the standard error (stderr) into stderr.txt. This way, normal output and error messages are separately stored in distinct files for further examination or processing.
