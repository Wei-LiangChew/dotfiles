# dotfiles
For my personal configurations

## Set up steps:

1. Clone the repo into the user directory where the configuration needs to be applied:

```
git clone git@github.com:Wei-LiangChew/dotfiles.git
```

Note: might need to set up git SSH keys or other form of login in order to clone.

2. Apply the configuration files:

```bash
ln -s dotfiles/.myvimrc ~/.vimrc
ln -s dotfiles/.gitignore_global ~/.gitignore_global
ln -s dotfiles/.tmux.conf ~/.tmux.conf

cp dotfiles/.gitconfig ~/.gitconfig
# hard copy required to allow git to work in the `dotfiles` directory
```

In the case of the `.gitconfig` file, you might have to delete any existing one. Compare before doing so to make sure you don't delete anything by mistake.
In the case of the `.vimrc` file, it's using [vim-plug](https://github.com/junegunn/vim-plug) as a plugin manager. This needs to be installed, which requires some lines in `.myvimrc` to be uncommented temporarily.
