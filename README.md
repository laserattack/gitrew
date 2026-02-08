# Wtf?

**gitrew** (gitrewind) - simple Git wrapper that creates a snapshot of a Git repository at a specific point in time. The snapshot contains all files as they existed at that moment

# Usage

```
Usage: gitrew [-hlcb] timestamp
Flags:
  -h, --help     Show this help message and exit
  -l, --list     Show snapshots (~/.gitrewind dir by default) end exit
  -c, --cleanup  Delete all snapshots (~/.gitrewind dir by default)
  -b, --branch   Specify a Git branch (otherwise, the current one is used)
Examples:
  gitrew 2 weeks ago
  gitrew -b master 2 minute ago
  gitrew 2026-02-08 15:52
Warning: Git's date parser is very strange. 'gibberish' may return
         the latest commit. Use proper timestamps e.g. like above.
```

# Requirements

- Perl 5.10+
- Git
- some standard unix utils
