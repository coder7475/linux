# Process Monitoring

A process is an instance of a computer program that is being executed. Each process is identified by a unique number called a process ID (**PID**).
Several process can make up a service.

There are several linux command to monitor process:

- `ps` - report a snapshot of the current processes
- `top` - display Linux processes in real time
- `htop` - interactive process viewer
- `atop` - advance interactive monitor to view the load on linux system
- `lsof` - list open files

## ps

- `ps`: Displays processes for the current shell session
- `ps -ef`: Display all the process running ont the machine in full-format listing
- `ps aux`: Display detailed information about all currently running processes, including those run by other users.
- `ps AFL`: Display snapshot of all currently running process in a full format listing
- `ps -u <username>`: Displays processes for a specific user.
