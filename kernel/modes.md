# Types of Modes

PC and Server generally has two modes:

1. Kernel Mode
2. User Mode

# User Mode

- process in user mode are said to be in **userland** - user space
- process operates in user mode and can't access device
- processes indirectly access deivices through kernel
- uses `system calls` to request kernel to perform tasks

# Kernel Mode

- kernel operates in kernal mode and can access devices.

# Examples of System Calls

- Creating and deleting processes
- Allocating and deallocating memory
- Communication processing
- File system operations
- Device operations

# Commands for System Calls

```bash
strace
```
