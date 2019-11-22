# System Calls Assignment

### Objective
The goal of this week's assignment is to make you familiar with the Unix form of documentation of system calls via manpages.

### Documentation
## System Calls Understanding

+ fork: It creates a new process of the calling process

  Arguments: No arguments available.
+ stat: It displays files or the file system status.

  Arguments: -L = dereference; --f = file-system; -c = specified FORMAT, --printf = like --format but interpret backslash escapes, and do not output a mandatory trailing newline; and FILE.

+ kill: It sends a signal to the process, given in the parameters, to terminate the process immediately.

Arguments: [OPTIONS] -L = --table; -l = --list = Lists signal names; --signal = specific signal to send; <pid>.

+ mmap: creates  a  new  mapping  in  the  virtual address space of the calling process.

Arguments: void* addr, size_t length, int prot, int flags, int fd, off_t offset

+ chmod: The command changes the permissions for files and directorys, in order limit access for a specific user or group.

Arguments: [OPTIONS] MODE FILE, OCTAL-MODE FILE, --reference=RFILE FILE

+ waitpid: With the given process ID, it waits for the Process to change his actual state.

Arguments: waitpid(pid_t pid, int* wstatus, int options) or waitpid(int* wstatus).


## System Calls Fails
Applies to all commands in this task!
All have an error for "File don't exists"!

fork: Fails when the system, doesn't have enough memory.

exec: Fails when it doesn't have execute permissions or the file dont't exists.

unlink: Fails when the pathname is out of the accesible path.

read: Fails when you don't have the permission to read a file.

mount: Fails when a component doesn't exist.

chmod: Fails when you don't have permissions or when the file doesn't exist.

kill: Fails when the process don't have permissions for killing other process or the other process doesn't exists.


A Trap instruction can be activated by a division by zero or invalid memory access.
It's a command to switch from the user mode to kernel mode, because system calls work
with a much higher priority than user code.
So the program is able to kill the process if the program would trigger an unhandled Exception in his code. 
