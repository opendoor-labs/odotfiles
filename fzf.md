# [`fzf`](https://github.com/junegunn/fzf) 🌸

fzf enables interactive fuzzy filtering of a list of strings (file paths, lines of code, git commits, etc.) with previews

See longer explainer [here](https://gist.github.com/nathanshelly/4b7020d09d413cab823914b06162145a#-fzf).

## keybindings

> Note: You will likely need to change a setting in your terminal emulator to enable keybindings containing `Option`. See [the appendix below](#enabling-keybindings) for instructions that should take ~30 seconds.

> Note II: these bindings configured in [`$DOTFILES/zsh/fzf.zsh`](#fzf.zsh)

> Note III: below `C` means `Ctrl`, and `M` means `Option` (on macOS) or `Alt` (on Windows)

- `C-g` - filter and output files from the root of the current git repo
- `C-t` - filter and output files below current directory
- `C-p` - filter and edit files below current directory (same files listed by `C-t`). Files edited via `$EDITOR` (configured in [`.files-settings.json`](.files-settings.json)).
- `C-r` (or `/` in `vicmd` (normal) mode) - filter and run shell history. Hit `C-e` instead of `Enter` to output the command to the line for editing before running.
- `M-c` - filter and `cd` to directories below the current directory. If you have part of a command typed this will preserve that command while switching directories.

### `git` bindings

> Note: these bindings configured in [`$DOTFILES/zsh/git.zsh`](./zsh/fzf_git.zsh)

- `M-f` - filter and output files shown by `git status` (untracked, unstaged, staged) to shell
- `M-t` - filter `git log` commits and output hash to shell
- `M-r` - filter all (local and remote) git branches and output to shell

## configuration

Use `fd` (instead of default `find`) for `**` path & directory completion and keybindings.

Enable multi-select (w/ `Tab` & `Shift-Tab`) by default. Use `Ctrl-a` to select all filtered values. Use `Ctrl-k` & `Ctrl-l` to move down and up results list.

Add previews w/ `bat` (toggleable w/ `Ctrl-Space`). Use `Ctrl-d` & `Ctrl-u` to scroll previews down and up, respectively.

## aliases

Two aliases defined in [`$DOTFILES/zsh/alias.zsh`](./zsh/alias.zsh):

- `rgz <query>` - filter and open lines matching `<query>`
- `killp <port>` - filter and kill processes running on the given port

## functions

See [`$DOTFILES/functions/fzf/README.md`](./functions/fzf/README.md).

## appendix

### enabling keybindings

Various terminals on macOS require brief configuration in order to use keybindings containing `Option`.

#### "Terminal" - default macOS terminal

Tick the box labeled "Use Option as Meta key" in Profiles > Keyboard.

![Terminal](https://user-images.githubusercontent.com/9750687/74061402-cb24c100-49a0-11ea-9270-2707170cc592.png 'terminal')

#### iTerm

Select "Esc+" for "Left ⌥ Key" & "Right ⌥ Key" in Profiles > Keys.

![iTerm](https://user-images.githubusercontent.com/9750687/74061408-ceb84800-49a0-11ea-90ec-c7cab978a15c.png 'iTerm')

#### Alacritty

Copy and paste [these bindings](https://github.com/nathanshelly/.files/blob/ba5fc4e/gui/apps/alacritty/alacritty.yml#L632-L705) into your `alacritty.yml`.
