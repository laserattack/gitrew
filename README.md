# Wtf?

**gitrew** (gitrewind) - simple Git wrapper that creates a snapshot of a Git repository at a specific point in time. The snapshot contains all files as they existed at that moment

# Usage

```
Usage: gitrew [-hlcib] timestamp
Flags:
  -h, --help         Show this help message and exit
  -l, --list         Show memories (~/.gitrewind dir by default) end exit
  -c, --cleanup      Delete memories (~/.gitrewind dir by default)
  -i, --interactive  Interactive mode (u need fzf for use it)
  -b, --branch       Specify a Git branch (otherwise, the current one is used)
Examples:
  gitrew 2 weeks ago
  gitrew -b master 2 minute ago
  gitrew 2026-02-08 15:52
  gitrew -b main -i
Warning: Git's date parser is very strange. 'gibberish' may return
         the latest commit. Use proper timestamps e.g. like above.
```

# Requirements

- Perl 5.10+
- Git
- fzf (optional, for interactive mode)
- some standard unix utils
