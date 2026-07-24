# Day 29 of Cisco Linux Essentials Course

Today I covered Section 5.5: Command Types — learning how Bash decides what to execute when a command is entered.

## Internal vs External Commands

**Internal (Built-ins)** like `cd` and `pwd` are loaded directly into RAM along with the shell process. They execute instantly and never need to search `$PATH`.

**External** commands like `ls`, `grep`, and `python3` are executable files stored in directories like `/usr/bin`. Bash uses `$PATH` to search for them, directory by directory.

## Diagnostic Tools: type vs which

- `which` — only searches `$PATH` for the binary file
- `type` — tells you the exact nature of a command: Built-in, External, Alias, or Function
- `type -a` — shows every existing version of a command at once (e.g., `echo` exists both as a shell builtin and as a `/bin/echo` binary)

## Aliases vs Functions

- **Aliases** (`alias c='clear'`) — single-line shortcuts
- **Functions** (`sys_cleanup () { ... }`) — mini-scripts that run multiple complex commands sequentially with a single call

**Persistence note:** Custom aliases and functions created in a session are temporary. To make them permanent across reboots, add them to shell initialization files like `.bashrc`.

Tested hands-on on my AWS EC2 instance.

#Linux #DevOps #CiscoNetworkingAcademy #LearningInPublic #Bash
