# Script to get a password from `pass` through `tmux`, using `fzf`

### To use:

Clone the repo:
```
git clone https://github.com/hughdavenport/passmux
```

Create keybinding tmux:

```
bind-key    -T prefix C-p              run-shell "~/passmux/passmux --type"
```

Make sure you have [tmux](https://github.com/tmux/tmux), [fzf](https://github.com/junegunn/fzf) and [keychain](https://github.com/funtoo/keychain) installed, or edit the script to suit.

Make sure keychain knows about your gpg key (ie in your bashrc, zshrc, etc).

Run ssh-add or similar, then hit prefix C-p, then select the password, then enter in GPG passphrase. It should type to current pane.

Remove the --type option in the binding to copy to clipboard.


This was adapted from the contrib passmenu script for dmenu integration.

## Copyright

©2016 Hugh Davenport, All The Things Ltd under MIT license
