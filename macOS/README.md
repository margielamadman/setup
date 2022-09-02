# macOS Setup

## Ansible tags
Use tags by passing the `--tags` flag to `ansible-playbook`
* `install` - everything
* `core` - majority of system programs
* `zsh` - setup zsh
* `vim` - setup neovim and plugin dependencies
* `dotfiles` - get dotfiles

## After install
* Run `:PlugInstall` to install neovim plugins
* Run `:TSUpdate` to install treesitter parsers
