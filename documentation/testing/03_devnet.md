---
id: devnet
title: Running a Local Devnet
sidebar_label: Devnet
---

A local devnet can be a heavyweight but reliable way to test your application on Aleo.

## Setup

To run a local devnet, you'll need to install [snarkOS](https://developer.aleo.org/guides/introduction/getting_started#2-installing-snarkos).
You'll also need `tmux` (instructions below) and the [devnet.sh](https://github.com/ProvableHQ/snarkOS/blob/staging/devnet.sh) script in the `snarkOS` repository.

<details><summary>macOS</summary>

To install `tmux` on macOS, you can use the `Homebrew` package manager.
If you haven't installed `Homebrew` yet, you can find instructions at [their website](https://brew.sh/).
```bash
# Once Homebrew is installed, run:
brew install tmux
```

</details>

<details><summary>Ubuntu</summary>

On Ubuntu and other Debian-based systems, you can use the `apt` package manager:
```bash
sudo apt update
sudo apt install tmux
```

</details>

<details><summary>Windows</summary>

There are a couple of ways to use `tmux` on Windows:

## Using Windows Subsystem for Linux (WSL)

1. First, install [Windows Subsystem for Linux](https://docs.microsoft.com/en-us/windows/wsl/install).
2. Once WSL is set up and you have a Linux distribution installed (e.g., Ubuntu), open your WSL terminal and install `tmux` as you would on a native Linux system:
```bash
sudo apt update
sudo apt install tmux
```

</details>

### Runing the Devnet

Run the `devnet.sh` script and follow the prompts.

`tmux` allows you to toggle between nodes in your local devnet. Here are some useful (default) commands:

```bash
# To toggle to the next node in a local devnet
Ctrl+b n 
# To toggle to the previous node in a local devnet
Ctrl+b p 
# To scroll easily, press q to quit
Ctrl+b [ 
# To select a node in a local devnet
Ctrl+b w 
# To select a node manually in a local devnet
Ctrl+b :select-window -t {NODE_ID}
# To stop a local devnet
Ctrl+b :kill-session
```
