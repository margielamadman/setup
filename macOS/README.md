# macOS Setup

## Ansible tags
Use tags by passing the `--tags` flag to `ansible-playbook`
* `install` - everything
* `core` - majority of system programs
* `zsh` - install and setup zsh
* `vim` - install and setup neovim
* `dotfiles` - get dotfiles

## After install
* Run `:PlugInstall` to install neovim plugins
* Run `:TSUpdate` to install treesitter parsers
