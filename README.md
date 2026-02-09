# Wtf?

**gitrew** (gitrewind) - simple Git wrapper that creates a snapshot of a Git repository at a specific point in time. The snapshot contains all files as they existed at that moment

# Usage

```
Usage: gitrew [-lcb] timestamp
Flags:
  -l, --list     Show all snapshots (~/.gitrewind dir) and exit
  -c, --cleanup  Delete all snapshots (~/.gitrewind dir) and exit
  -b, --branch   Specify a Git branch (otherwise, the current one is used)
Examples:
  gitrew 2 weeks ago
  gitrew -b master 2 minute ago
  gitrew 2026-02-08 15:52
Warning: Git's date parser is very strange. 'gibberish' may return
         the latest commit. Use proper timestamps e.g. like above
```

You can also add this function

``` bash
grcd() { local d; d=$(gitrew "$@" 2>/dev/null) && cd "$d" 2>/dev/null; }
```

to your `~/.bashrc` to quickly switch to a past version of the repository

```
~/projects/gitrew
[serr@lap]-> grcd 5 hour ago
~/.gitrewind/gitrew_1770631861/gitrew
[serr@lap]->
```

# Requirements

- linux system
- Perl 5.10+
- Git
- some standard unix utils
