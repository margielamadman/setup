# Ubuntu Setup

## Ansible tags
Use tags by passing the `--tags` flag to `ansible-playbook`
* `install` - everything
* `core` - majority of system programs
* `zsh` - install and setup zsh
* `vim` - install and setup neovim
* `brave` - install brave
* `spotify` - install spotify
* `pass` - install 1password
* `dotfiles` - get dotfiles

## After install
* Run `:PlugInstall` to install neovim plugins
* Run `:TSUpdate` to install treesitter parsers
