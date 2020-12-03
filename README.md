# gitconfig

My personal git configuration being used on my laptop as well as on servers I
have to deal with.

# Features
* colours everywhere
* many aliases to save your fingers!
* using vim for diff and merges
* git-sh-prompt setup

# Installation

The .gitconfig `[include]` syntax requires Git 1.7.10+. Though it is
recommended to use the [latest stable version](https://launchpad.net/~git-core/+archive/ubuntu/ppa) if possible.

* Download or clone the repository to some directory (e.g. `~/github/porn/gitconfig/`).
```
cd ~
mkdir -p github/attawayinc
cd github/attawayinc
git clone https://github.com/attawayinc/gitconfig.git
```

* Include the gitconfig file in your `~/.gitconfig`:
```
[include]
	path = ~/github/attawayinc/gitconfig/gitconfig
...
```
This way your local changes won't overwrite the file when you use:
```
git config --global user.name "AttawayInc"
git config --global user.email "mattaway6@student.wgu.edu"
```

* Include the git prompt config in your `~/.bashrc`:
```
$ echo "source ~/github/attawayinc/gitconfig/bashrc.gitprompt" >> ~/.bashrc
```
On next login your bash prompt will show nice symbols that represent the state
of your current working tree. If you want to enable git prompt without logging
out and in, just source the file:
```
$ source ~/github/attawayinc/gitconfig/bashrc.gitprompt
```
