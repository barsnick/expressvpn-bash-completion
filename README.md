# ExpressVPN Bash Completion for `expressvpnctl`

Bash completion for Linux (Bash 4+), targeting the ExpressVPN CLI executable
`expressvpnctl`.

For ExpressVPN client versions up to 3, Bash completions were included.

Created and tested against ExpressVPN client `expressvpnctl` version
`5.0.1+11498`.

## Features

- Completes top-level commands and global flags from `expressvpnctl --help`.
- Completes `set`, `get`, and `monitor` subtypes and enum values.
- Dynamically completes available regions at tab time via
  `expressvpnctl get regions`.
- Supports `connect` and `set region` with dynamic regions and `smart`.
- Completes file arguments for `login` and split-tunnel app rules.

## Installation (System-wide)

1. Copy the completion file to the system bash-completion directory:
   ```bash
   sudo install -m 0644 expressvpnctl /etc/bash_completion.d/expressvpnctl
   ```
2. Start a new shell session (or `source /etc/bash_completion`).

## Installation (User-only)

1. Ensure the user completions directory exists:
   ```bash
   mkdir -p ~/.local/share/bash-completion/completions
   ```
2. Copy the completion file:
   ```bash
   install -m 0644 expressvpnctl ~/.local/share/bash-completion/completions/expressvpnctl
   ```
3. Start a new shell session (or `source ~/.bashrc` if it loads bash-completion).
