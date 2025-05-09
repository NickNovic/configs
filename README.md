# Dotfiles

My personal dotfiles for a minimal and productive development environment on Debian (with i3, Neovim, etc.).

---

## 📁 Contents

- `~/nvim` — Neovim configuration (Lua)
- `~/i3` — i3 window manager config

---

## 🚀 Setup Instructions (Debian)

### 1. Clone the Repo

```bash
git clone https://github.com/NickNovic/dotfiles.git ~/dotfiles
cd ~/dotfiles
````

### 2. Symlink Config Files

```bash
ln -s ~/dotfiles/nvim ~/.config/nvim
ln -s ~/dotfiles/i3 ~/.config/i3
```

### 3. Install Required Packages

```bash
sudo apt update
sudo apt install neovim clangd ripgrep fd-find build-essential
```

#### Fix fd symlink (Telescope compatibility)

```bash
mkdir -p ~/.local/bin
ln -s $(which fdfind) ~/.local/bin/fd
echo 'export PATH="$HOME/.local/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```

---

## 🛠 Neovim Setup

Open Neovim and run:

```vim
:PackerSync
:TSInstall c cpp
```

Optional:

```vim
:checkhealth
```

---

## 💾 Tools I Use

* **i3wm** — Tiling window manager
* **Neovim** — Code editor
* **Packer** — Plugin manager
* **nvim-cmp + clangd** — C/C++ autocompletion
* **Telescope** — Fuzzy finder
* **LuaSnip** — Snippet engine
* **Treesitter** — Syntax highlighting
