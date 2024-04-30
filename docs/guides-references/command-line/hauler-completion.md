---
title: Hauler Completion (Command)
description: Hauler CLI Reference for hauler completion
sidebar_label: Hauler Completion
---

### Command Overview

* The completion command generates completion scripts for various shells.

```yaml
Usage:
  hauler completion [command]

Available Commands:
  bash        Generates bash completion scripts
  fish        Generates fish completion scripts
  powershell  Generates powershell completion scripts
  zsh         Generates zsh completion scripts

Flags:
  -h, --help   help for completion

Global Flags:
  -l, --log-level string    (default "info")

Use "hauler completion [command] --help" for more information about a command.
```


#### `hauler completion bash`:

* The completion command generates completion scripts for bash.

```yaml
Usage:
  hauler completion bash [flags]

Examples:
To load completion run

        . <(hauler completion bash)

        To configure your bash shell to load completions for each session add to your bashrc

        # ~/.bashrc or ~/.profile
        command -v hauler >/dev/null && . <(hauler completion bash)

Flags:
  -h, --help   help for bash

Global Flags:
  -l, --log-level string    (default "info")
```

#### `hauler completion fish`:

* The completion command generates completion scripts for fish.

```yaml
Usage:
  hauler completion fish [flags]

Examples:
To configure your fish shell to load completions for each session write this script to your completions dir:

        hauler completion fish > ~/.config/fish/completions/hauler.fish

        See http://fishshell.com/docs/current/index.html#completion-own for more details

Flags:
  -h, --help   help for fish

Global Flags:
  -l, --log-level string    (default "info")
```

#### `hauler completion powershell`:

* The completion command generates completion scripts for powershell.

```yaml
Usage:
  hauler completion powershell [flags]

Examples:
To load completion run

        . <(hauler completion powershell)

        To configure your powershell shell to load completions for each session add to your powershell profile

        Windows:

        cd "$env:USERPROFILE\Documents\WindowsPowerShell\Modules"
        hauler completion powershell >> hauler-completion.ps1

        Linux:

        cd "${XDG_CONFIG_HOME:-"$HOME/.config/"}/powershell/modules"
        hauler completion powershell >> hauler-completions.ps1

Flags:
  -h, --help   help for powershell

Global Flags:
  -l, --log-level string    (default "info")
```

#### `hauler completion zsh`:

* The completion command generates completion scripts for zsh.

```yaml
Usage:
  hauler completion zsh [flags]

Examples:
To load completion run

        . <(hauler completion zsh)

        To configure your zsh shell to load completions for each session add to your zshrc

        # ~/.zshrc or ~/.profile
        command -v hauler >/dev/null && . <(hauler completion zsh)

        or write a cached file in one of the completion directories in your ${fpath}:

        echo "${fpath// /\n}" | grep -i completion
        hauler completion zsh > _hauler

        mv _hauler ~/.oh-my-zsh/completions  # oh-my-zsh
        mv _hauler ~/.zprezto/modules/completion/external/src/  # zprezto

Flags:
  -h, --help   help for zsh

Global Flags:
  -l, --log-level string    (default "info")
```
