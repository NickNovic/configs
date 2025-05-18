# Neovim Plugin Dependencies (Debian)

This README lists the required dependencies for the following Neovim plugins:

- Packer
- nvim-treesitter
- nvim-lspconfig (with Clangd for C/C++)
- nvim-cmp
- LuaSnip
- Telescope

---

## ✅ System Requirements

Make sure you're using **Neovim ≥ 0.8**.

### Install Neovim (if needed)
```bash
sudo apt update
sudo apt install neovim
````

---

## 📦 Install Required Packages

### 1. Compiler tools for Treesitter

```bash
sudo apt install build-essential
```

### 2. C/C++ Language Server (Clangd)

```bash
sudo apt install clangd
```

You may also want to set a symlink if the executable is not named `clangd`:

```bash
sudo ln -s /usr/bin/clangd-XX /usr/bin/clangd
# Replace XX with your installed version (e.g. clangd-14)
```

### 3. Search tools for Telescope

```bash
sudo apt install ripgrep fd-find
```

### 4. Search tools for Telescope

```bash
sudo apt install xclip 

```bash
mkdir -p ~/.local/bin
ln -s $(which fdfind) ~/.local/bin/fd
echo 'export PATH="$HOME/.local/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```

---

## ✅ Final Setup Steps

1. Open Neovim:

```bash
nvim
```

2. Run:

```vim
:PackerSync
:TSInstall c cpp
```

3. Optional: Run diagnostics

```vim
:checkhealth
```

---

## 🔧 Notes

* `clangd` enables smart autocompletion for C/C++.
* `ripgrep` and `fd` are used by Telescope for file searching.
* `build-essential` ensures Treesitter can compile parsers.
