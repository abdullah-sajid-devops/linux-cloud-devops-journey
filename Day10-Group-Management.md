# Day 10: Linux Group Management Commands 👥

## Overview
Practiced 7 essential Group Management Commands hands-on
on a live Ubuntu Server as part of my
100 Days DevOps & Cloud Engineering Challenge.

---

## Commands Mastered Today

| # | Command | Description | Hands-on Example |
|---|---------|-------------|------------------|
| 1 | `groupadd` | Create a new group | `groupadd developers` |
| 2 | `groupdel` | Delete an existing group | `groupdel developers` |
| 3 | `groupmod` | Modify existing group settings | `groupmod -n newname oldname` |
| 4 | `groups` | Show all groups a user belongs to | `groups username` |
| 5 | `gpasswd` | Manage group members & password | `gpasswd -a username groupname` |
| 6 | `grpck` | Verify integrity of group files | `grpck` |
| 7 | `grpconv` | Convert group file to shadow groups | `grpconv` |

---

## Key Learnings

- **`groupadd`** — First step in group management.
  Always create a group before adding users to it.
- **`gpasswd -a`** — Adds a user to a group.
  `-a` means append — without it, user gets replaced!
- **`gpasswd -d`** — Removes a user from a group.
  Essential for revoking access quickly.
- **`groups`** — Quick way to check which groups
  a user belongs to. Great for debugging permission issues.
- **`grpck`** — Verifies group file integrity.
  Run this after manual edits to `/etc/group`.
- **`grpconv`** — Converts to shadow group passwords
  for extra security layer beyond standard groups.
- **Real World Use:** Instead of setting permissions
  for each user individually — add them to a group
  and manage access once for everyone. This is how
  real production servers are managed!

---

## Group Management Workflow

Create Group → Add Users → Set Permissions → Verify
groupadd      gpasswd -a   chmod/chgrp      groups/grpck

---

## User vs Group Management

| Task | User Command | Group Command |
|------|-------------|---------------|
| Create | `useradd` | `groupadd` |
| Delete | `userdel` | `groupdel` |
| Modify | `usermod` | `groupmod` |
| Password | `passwd` | `gpasswd` |
| Verify | `id` | `grpck` |

---

## Environment
- **OS:** Ubuntu Server (AWS EC2)
- **Source:** GeeksForGeeks Linux Track
- **Status:** ✅ All commands practiced on live terminal

---

*Part of my 100 Days DevOps & Cloud Engineering Challenge*
*Follow my journey: [LinkedIn](https://www.linkedin.com/in/abdullah-sajid-azure)*
