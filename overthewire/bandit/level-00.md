# Bandit Level 0 → 1

## Goal
Log in to the game server over SSH and find the password for the next level, stored in a file called `readme` in the home directory.

## What I tried
Connected with SSH on the non-default port, then listed the home directory to see what was there.

```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
ls -la
```

## Solution

```bash
cat readme
# password: <redacted>
```

## What I learned
- `ssh user@host -p PORT` connects to a remote machine on a specific port.
- `ls -la` shows every file, including hidden ones, with permissions and owner.
- `cat` (short for *concatenate*) prints a file's contents to the terminal.
