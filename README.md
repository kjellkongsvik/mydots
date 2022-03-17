---
marp: true
---
# dotfiles: Keep your ~ settings

`https://github.com/<user>/dotfiles`

 - .bashrc
 - .vimrc
 - .config/alacritty.json
 - .config/Code/User/settings.json

`install.sh`:
```
#!/usr/bin/env bash
export DEST=$HOME
find . -type d -not -path "./.git*" -exec mkdir -p $DEST/{} \;
find . -type f -not -path "./.git/*" -not -path "./install.sh" -exec ln -s $PWD/'{}' $DEST/'{}' \;
```
---
# Some other setups

## A bare Git repository

https://www.atlassian.com/git/tutorials/dotfiles

## yadm

https://yadm.io

---

# GitHub Codespaces

https://dotfiles.github.io/

Automatically creates symlinks of the dotfiles into the codespace.

If you have folders, you need a script like `install.sh`

https://docs.github.com/en/codespaces/customizing-your-codespace/personalizing-codespaces-for-your-account

---

https://github.com/kjellkongsvik/mydots/
