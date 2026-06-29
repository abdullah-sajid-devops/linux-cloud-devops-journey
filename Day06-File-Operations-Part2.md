# Day 6: Linux File Operational Commands — Part 2 🐧

## Overview
Completed the remaining 20 File Operational Commands hands-on
on a live Ubuntu Server. This completes the full 40-command
File Operations module from GeeksforGeeks.

---

## Commands Mastered Today

| # | Command | Description | Hands-on Example |
|---|---------|-------------|------------------|
| 21 | `look` | Display lines starting with given string | `look "#include" file.c` |
| 22 | `more` | View file content page by page (basic) | `more sample.txt` |
| 23 | `mv` | Move or rename files/directories | `mv old.txt new.txt` |
| 24 | `od` | Display file in octal/other formats | `od file.txt` |
| 25 | `paste` | Merge files horizontally line by line | `paste a.txt b.txt` |
| 26 | `readlink` | Show target path of symbolic link | `readlink link.txt` |
| 27 | `rename` | Bulk rename files using patterns | `rename 's//.log/' *.txt` |
| 28 | `rev` | Reverse characters in each line | `rev file.txt` |
| 29 | `rm` | Delete files permanently | `rm file.txt` |
| 30 | `shred` | Securely delete files (unrecoverable) | `shred demo.txt` |
| 31 | `sort` | Sort lines alphabetically or numerically | `sort file.txt` |
| 32 | `split` | Split large file into smaller parts | `split demo.txt part_` |
| 33 | `tac` | Display file content in reverse order | `tac file.txt` |
| 34 | `tail` | Show last lines of a file (live monitoring) | `tail -f file.txt` |
| 35 | `tar` | Create/extract archive files for backup | `tar -cvf archive.tar files/` |
| 36 | `tee` | Write output to both file and terminal | `echo "Hello" \| tee demo.txt` |
| 37 | `touch` | Create empty file or update timestamp | `touch test.txt` |
| 38 | `unexpand` | Convert spaces into tabs | `unexpand file.txt` |
| 39 | `uniq` | Remove duplicate lines from file | `uniq file.txt` |
| 40 | `wc` | Count lines, words, and characters | `wc file.txt` |

---

## Key Learnings

- **`tail -f`** — Live log monitoring in real time.
  Every DevOps Engineer uses this daily for debugging
  production servers.
- **`rm` vs `shred`** — `rm` deletes file but data can be
  recovered. `shred` overwrites data multiple times —
  use for sensitive files.
- **`tac` vs `cat`** — `cat` reads top to bottom,
  `tac` reads bottom to top. Useful for log analysis.
- **`tar`** — Most important archiving tool in Linux.
  Used everywhere in DevOps for backups and deployments.
- **`sort` + `uniq`** — Powerful combo for data processing
  and removing duplicates from log files.
- **`tee`** — Great for logging pipeline output while
  still seeing it on screen.

---

## Module Complete! ✅

All 40 File Operational Commands finished across Day 5 & Day 6.

| Days | Commands Covered |
|------|-----------------|
| Day 5 | Commands 1-20 (basename to locate) |
| Day 6 | Commands 21-40 (look to wc) |

---

## Environment
- **OS:** Ubuntu Server (AWS EC2)
- **Source:** GeeksForGeeks Linux Track
- **Status:** ✅ All commands practiced on live terminal

---

*Part of my 100 Days DevOps & Cloud Engineering Challenge*
*Follow my journey: [LinkedIn](https://www.linkedin.com/in/abdullah-sajid-devops)*
