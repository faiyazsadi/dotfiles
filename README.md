# Dotfiles Setup with GNU Stow

This repository contains my dotfiles, which are managed using [GNU Stow](https://www.gnu.org/software/stow/). Follow the instructions below to easily set up the same configuration on a new machine.

## Prerequisites

Before using the dotfiles, ensure that `stow` is installed. You can install it using your package manager:

### For Debian/Ubuntu:

```bash
sudo apt-get install stow
```

## Directory Structure

This repository is organized into subdirectories, each representing a different configuration (e.g., `tmux`, `bash`, `vim`, etc.). Each subdirectory contains the dotfiles specific to that tool.

For example:

```
dotfiles/
│
├── bash/       # Contains .bashrc, .bash_profile, etc.
├── vim/        # Contains .vimrc, etc.
├── tmux/       # Contains .tmux.conf, etc.
└── ...
```

## How to Use

1. **Clone this repository to your home directory**:

   ```bash
   git clone https://github.com/your-username/dotfiles.git ~/dotfiles
   ```

2. **Navigate to the dotfiles directory**:

   ```bash
   cd ~/dotfiles
   ```

3. **Stow the desired configurations**:

   Use `stow` to symlink the desired configuration files to your home directory. For example:

   - To set up the `bash` configuration:

     ```bash
     stow bash
     ```

   - To set up the `vim` configuration:

     ```bash
     stow vim
     ```

   - To set up all configurations at once:

     ```bash
     stow *
     ```

   This will create symlinks in your home directory, pointing to the dotfiles in this repository.

4. **Unstow a configuration (optional)**:

   If you want to remove the symlinks for a specific configuration, use the `-D` flag with `stow`:

   ```bash
   stow -D vim
   ```

## Adding New Dotfiles

To add new dotfiles:

1. Place the new configuration files in an appropriately named subdirectory (e.g., `zsh/` for `.zshrc`).
2. Stow the new configuration as described above.
