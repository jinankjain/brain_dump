## Namespaces in Linux

- Provides isolation of shared resources: each application unique view of system
- For example: Docker uses namespaces to provide each container its filesystem and network
- Linux also offers PID namespaces

## Pids in Linux
- Hierarchical structure and each process does have a unique PID
- `fork()` returns the PID of child process to the parent process
- PID 1 refers to `init` process also the root of the userspace process tree.
- If PID 1 dies kernel panics and you will need a reboot

## Pid Namespaces
- First process created after `unshare` syscall will have PID 1 in this new namespace
