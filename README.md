# Usage

```
Usage: gitrew [-hci] timestamp
Flags:
  -h, --help         Show this help message and exit
  -c, --cleanup      Delete memories (~/.gitrewind dir by default) and exit
  -i, --interactive  Interactive mode (u need fzf for use it)
Examples:
  gitrew 2 weeks ago
  gitrew 2 minute ago
  gitrew 2026-02-08 15:52
  gitrew -i
```