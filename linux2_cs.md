SSH generation
--------------

sh-keygen -t rsa -C "your_email@example.com"
```
	Creates a new ssh key, using the provided email as a label
	Generating public/private rsa key pair.
	Enter file in which to save the key (/home/you/.ssh/id_rsa):

	Enter passphrase (empty for no passphrase): [Type a passphrase]
	Enter same passphrase again: [Type passphrase again]

	Your identification has been saved in /home/you/.ssh/id_rsa.
	Your public key has been saved in /home/you/.ssh/id_rsa.pub.
	The key fingerprint is:
	01:0f:f4:3b:ca:85:d6:17:a1:7d:f0:68:9d:f0:a2:db your_email@example.com
```

start the ssh-agent in the background
eval "$(ssh-agent -s)"
	Agent pid 59566
ssh-add ~/.ssh/id_rsa


ssh -T git@github.com
# Attempts to ssh to GitHub


"The authenticity of host 'github.com (207.97.227.239)' can't be established.
# RSA key fingerprint is 16:27:ac:a5:76:28:2d:36:63:1b:56:4d:eb:df:a6:48.
# Are you sure you want to continue connecting (yes/no)?


compile vim with python and other support
-----------------------------------------

#source: https://kowalcj0.wordpress.com/2013/11/19/how-to-compile-and-install-latest-version-of-vim-with-support-for-x11-clipboard-ruby-python-2-3/
# 
"install required packages
sudo apt-get install mercurial python python-dev python3 python3-dev ruby ruby-dev libx11-dev libxt-dev libgtk2.0-dev  libncurses5  ncurses-dev

sudo apt-get update --fix-missing	#if sth was not installed and install again

#download vim src
hg clone https://vim.googlecode.com/hg/ vim

"configure it 
./configure \
    --enable-pythoninterp \
    --enable-rubyinterp \
    --enable-cscope \
    --enable-gui=auto \
    --enable-gtk2-check \
    --enable-gnome-check \
    --with-features=huge \
    --enable-multibyte \
    --with-x \
    --with-compiledby="Senor QA <senor@qa>" \
    --with-python-config-dir=/usr/lib/python2.7/config-x86_64-linux-gnu

make
sudo make install
sudo apt-get install libclang-dev
