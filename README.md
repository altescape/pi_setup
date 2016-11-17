# pi_setup
Setup a new Raspberry Pi with latest Ruby, Vim, screen, etc

Need to move all this to ansible playbook (https://serversforhackers.com/an-ansible-tutorial)

```
apt install tmux
apt-get install zsh
apt install ncurses-dev
apt install libncurses5-dev libgnome2-dev libgnomeui-dev libgtk2.0-dev libatk1.0-dev libbonoboui2-dev libcairo2-dev libx11-dev libxpm-dev libxt-dev ruby-dev libperl-dev
apt install screen
apt install lua5.2-dev
apt install lua5.2 luajit
apt-get install python-dev
```

### install node

```
sudo apt-get install nodejs npm node-semver
```

### install rvm

see https://rvm.io/

```
gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3
curl -sSL https://get.rvm.io | bash -s stable
source /home/pi/.rvm/scripts/rvm
```

```
rvm list known
rvm install 2.3.2
```

### install vim

`apt-get remove vim-tiny vim-common vim-gui-common vim-nox`

`git clone https://github.com/vim/vim.git`

`cd vim`

```
 make distclean
 clear
 ./configure --with-features=huge --enable-cscope --enable-pythoninterp=yes --with-python-config-dir=/usr/lib/python2.7/config-x86_64-linux-gnu --enable-multibyte --enable-fontset --enable-gui=gnome2 --disable-netbeans --enable-luainterp=yes --with-lua-prefix=/usr/include/lua5.2 --enable-largefile --enable-rubyinterp
 sudo make
 sudo make install
 ```
