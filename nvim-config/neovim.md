# Neovim Setup on Ubuntu 24

## Requirements

- Ubuntu 24.04 LTS or later
- Git (for plugin management)
- Build tools (gcc, make, etc.)
- Python 3 and pip (for Python provider)
- Node.js and npm (for Node.js provider)
- Ripgrep (for faster searching)
- A Nerd Font (for icons in plugins)

## Installation

### Install Latest Stable Release (Recommended)

Download and install the latest stable release from the official repository:

```bash
# Install dependencies
sudo apt update
sudo apt install curl

# Download the latest stable release
curl -LO https://github.com/neovim/neovim/releases/latest/download/nvim-linux-x86_64.appimage
chmod u+x nvim-linux-x86_64.appimage
./nvim-linux-x86_64.appimage

# Expose nvim
sudo mkdir -p ~/opt/nvim
sudo mv nvim-linux-x86_64.appimage /opt/nvim/nvim

# Add nvim path to shell config
export PATH="$PATH:/opt/nvim/"
```

## Verify Installation

```bash
# Check Neovim version
nvim --version

# Check health of providers
nvim +checkhealth
```

## Configuration

Add Neovim configuration files at:
- `~/.config/nvim/`

Create the configuration directory if not exists:

```bash
mkdir -p ~/.config/nvim
```
