# Day 15: Linux Hardware & System Information Commands 🖥️

## Overview
Practiced 15 essential Hardware & System Information Commands
hands-on on a live Ubuntu Server as part of my
100 Days DevOps & Cloud Engineering Challenge.

---

## Commands Mastered Today

| # | Command | Description | Hands-on Example |
|---|---------|-------------|------------------|
| 1 | `acpi` | Display battery and power information | `acpi -V` |
| 2 | `acpi_available` | Check if ACPI is available | `acpi_available` |
| 3 | `acpid` | ACPI event daemon manager | `systemctl status acpid` |
| 4 | `arch` | Display system architecture | `arch` |
| 5 | `dmesg` | Display kernel ring buffer messages | `dmesg | tail -20` |
| 6 | `dmidecode` | Display hardware information from BIOS | `dmidecode -t memory` |
| 7 | `dstat` | Real-time system resource statistics | `dstat -cdngy` |
| 8 | `free` | Display memory usage | `free -h` |
| 9 | `hdparm` | Get/set hard disk parameters | `hdparm -I /dev/sda` |
| 10 | `hwclock` | Display or set hardware clock | `hwclock --show` |
| 11 | `iostat` | Display CPU and disk I/O statistics | `iostat -x 1` |
| 12 | `iotop` | Monitor disk I/O usage by process | `iotop` |
| 13 | `lsusb` | List USB devices connected to system | `lsusb` |
| 14 | `lshw` | Display detailed hardware information | `lshw -short` |
| 15 | `uname` | Display system and kernel information | `uname -a` |

---

## Key Learnings

- **`dmidecode`** — Most powerful command in this module.
  Shows complete hardware info — CPU, RAM slots,
  motherboard, BIOS version — without opening the server!
  Essential for remote server management.
- **`dmesg`** — First command to run when server has issues.
  Shows kernel messages and hardware errors in real time.
- **`free -h`** — Quick memory check.
  `-h` flag shows human readable format (GB/MB).
  Run this when server feels slow!
- **`uname -a`** — Shows kernel version, architecture,
  and OS info. Always run on a new server first!
- **`dstat`** — Better than vmstat and iostat combined.
  Shows CPU, disk, network, and memory all at once.
- **`iotop`** — Like `top` but for disk I/O.
  Find which process is killing your disk performance!
- **`lshw -short`** — Quick hardware summary.
  Shows all hardware in a clean table format.
- **`hwclock`** — Hardware clock vs system clock.
  Important for time sync on servers — wrong time
  can break SSL certificates and logs!

---

## System Diagnostics Workflow
New Server Checklist:
uname -a      → Check kernel & architecture
free -h       → Check available memory
df -h         → Check disk space
lshw -short   → Check all hardware
dmesg | tail  → Check for hardware errors
dmidecode     → Check BIOS & hardware details

---

## Hardware Info Commands Comparison

| Command | Shows | Best For |
|---------|-------|----------|
| `uname` | Kernel & OS info | Quick system check |
| `lshw` | All hardware | Complete hardware audit |
| `dmidecode` | BIOS & hardware | Remote hardware details |
| `lsusb` | USB devices | Peripheral management |
| `arch` | CPU architecture | Script compatibility |

---

## 15 Day Milestone ✅

**Half a month done — Zero days skipped! 🔥**

| Week | Topics Covered |
|------|---------------|
| Week 1 (Day 1-7) | IAM, Storage, FHS, CLI, File Ops x2, Directory Ops |
| Week 2 (Day 8-14) | Permissions, Users, Groups, Processes, Terminal, Jobs, Disk |
| Week 3 Start (Day 15) | Hardware & System Info |

---

## Environment
- **OS:** Ubuntu Server (AWS EC2)
- **Source:** GeeksForGeeks Linux Track
- **Status:** ✅ All commands practiced on live terminal

---

*Part of my 100 Days DevOps & Cloud Engineering Challenge*
*Follow my journey: [LinkedIn](https://www.linkedin.com/in/abdullah-sajid-azure)*
