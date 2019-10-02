# bin

Various setup scripts

- [`configure_macos_settings`](./configure_macos_settings) - set macOS configuration (currently unimplemented)
- [`install_bits_and_pieces`](./install_bits_and_pieces) - install various bits and pieces (e.g. adding `zsh` to `/etc/shells` then setting it as the login shell, updating submodules, installing [`zplugin`](https://github.com/zdharma/zplugin) and more)
- [`install_brew`](./install_brew) - install [Homebrew](https://brew.sh) and all formulas/casks specified in [`Brewfile`](../../Brewfile)
- [`install_language_servers`](./install_language_servers) - install [`bash-language-server`](https://github.com/mads-hartmann/bash-language-server) & [`rls`](https://github.com/rust-lang/rls) (for [`rust`](https://www.rust-lang.org)) language servers.
  - used with [`coc.nvim`](https://github.com/neoclide/coc.nvim) client (see [config](../../vim/coc.vim))
- [`setup_git_config`](./setup_git_config) - fill in [`gitconfig.local.symlink.example`](../../git/gitconfig.local.symlink.example) template
- [`symlink`](./symlink) - symlink files throughout `$DOTFILES` based on the scheme described [here](../symlink.md)
- [`uninstall_brew`](./uninstall_brew) - uninstall [Homebrew](https://brew.sh) (includes all installed casks)