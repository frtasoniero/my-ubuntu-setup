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

### Option 1: Install from Ubuntu Repository (Stable)

```bash
sudo apt update
sudo apt install neovim
```

### Option 2: Install Latest Stable Release (Recommended)

Download and install the latest stable release from the official repository:

```bash
# Install dependencies
sudo apt update
sudo apt install curl

# Download the latest stable release
curl -LO https://github.com/neovim/neovim/releases/latest/download/nvim-linux64.tar.gz

# Extract and install
sudo tar -C /opt -xzf nvim-linux64.tar.gz
sudo ln -sf /opt/nvim-linux64/bin/nvim /usr/local/bin/nvim

# Clean up
rm nvim-linux64.tar.gz
```

## Installing Additional Dependencies

### Python Provider

```bash
sudo apt install python3-pip
pip3 install --user pynvim
```

### Node.js Provider

```bash
# Install Node.js (using NodeSource)
curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo -E bash -
sudo apt install nodejs

# Install neovim npm package
sudo npm install -g neovim
```

### Ripgrep (for fast searching)

```bash
sudo apt install ripgrep
```

### Install a Nerd Font

```bash
# Download and install JetBrainsMono Nerd Font
mkdir -p ~/.local/share/fonts
cd ~/.local/share/fonts
curl -fLO https://github.com/ryanoasis/nerd-fonts/releases/latest/download/JetBrainsMono.zip
unzip JetBrainsMono.zip
rm JetBrainsMono.zip
fc-cache -fv
```

## Verify Installation

```bash
# Check Neovim version
nvim --version

# Check health of providers
nvim +checkhealth
```

## Configuration

Neovim configuration files are located at:
- `~/.config/nvim/init.lua` (Lua configuration)

Create the configuration directory:

```bash
mkdir -p ~/.config/nvim
```
