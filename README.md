
# livecmd
### ***livecmd***  is an enhanced command history viewer for Linux that organizes your command history in a more useful and readable format. It extends the functionality of the standard history command with powerful filtering, grouping, and display options.

## Features
**Alphabetical Grouping:** Commands are grouped by their first letter for quick scanning

**First-Letter Search:** Find commands by typing their starting letters

**Frequency Analysis:** View your most frequently used commands

**Timestamps:** Optionally display when commands were executed

**Colorized Output:** Easy-to-read color-coded display

**Flexible History Access:** View recent commands or your full history


## Usage

``livecmd [OPTIONS] [SEARCH_PATTERN]``

## Options

| Short Option | Long Option | Description |
|--------------|-------------|-------------|
| `-a` | `--all` | Show full command history (default: last 1000) |
| `-t` | `--time` | Show commands with execution timestamps |
| `-f` | `--frequent` | Show most frequently used commands |
| `-r` | `--recent` | Show recent commands (default) |
| `-h` | `--help` | Show help message |

## Examples

#### Show recent commands grouped by first letter:


``livecmd``

#### Show all commands starting with 'g':


``livecmd g``

#### Show all commands starting with 'git':


``livecmd git``

#### Show 20 most frequent commands:


``livecmd -f``

#### Show recent commands with timestamps:


``livecmd -t``

#### Show full command history:


``livecmd -a``

## Configuration
- You can customize the tool by modifying these variables at the top of the script:

- HISTORY_FILE: Path to your history file (default: ~/.bash_history)

- HISTORY_LENGTH: Number of recent commands to show by default (default: 1000)

- COLOR_* variables: Change color scheme

## Requirements
- Bash shell

- Standard GNU core utilities (awk, sort, grep, etc.)

- For timestamp support: properly configured HISTTIMEFORMAT

## Known Limitations

- Timestamps require proper HISTTIMEFORMAT configuration in bash

- Currently reads directly from history file rather than using history builtin

- Limited to bash history (may not work with zsh/fish without modification)

## Contributing

- Contributions are welcome! Please open issues or pull requests for:

- Bug fixes

- New features

- Support for other shells

- Improved performance
