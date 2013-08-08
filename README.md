dotfiles.git
============
Clone and run this on a new EC2 instance running Ubuntu 12.04.2 LTS to
configure your `bash` and `emacs` development environment as follows:

```sh
cd $HOME
git clone https://github.com/startup-class/dotfiles.git
ln -sb dotfiles/.screenrc .
ln -sb dotfiles/.bash_profile .
ln -sb dotfiles/.bashrc .
ln -sb dotfiles/.bashrc_custom .
mv .emacs.d .emacs.d~
ln -s dotfiles/.emacs.d .
```

See also http://github.com/startup-class/setup to install prerequisite
programs. If all goes well, in addition to a more useful prompt, now you can
do `emacs -nw hello.js` and hitting `C-c!` to launch an interactive SSJS
REPL, among many other features. See the
[Startup Engineering Video Lectures 4a/4b](https://class.coursera.org/startup-001/lecture/index)
for more details.

Addition for vim (per http://vim.wikia.com/wiki/Indenting_source_code ):

First enable file type detection with the following in your vimrc:
```sh
filetype plugin indent on
```

Create file html.vim with contents:
```sh
setlocal shiftwidth=2
setlocal tabstop=2
```

The html.vim file should be in this directory (which you may need to create):
~/.vim/after/ftplugin
