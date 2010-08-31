# Snakefire: Campfire Desktop client for Linux #

## LICENSE ##

Pyfire is released under the [MIT License] [license].

## INSTALLATION ##

### Requirements ###

### PyQT4 ###

The python library for QT integration is required.

For *Ubuntu based* systems, PyQT4 is in the official repositories, and can be
installed the following way:

		$ sudo apt-get install python-qt4

For *Arch Linux*, PyQT4 is in the extra repository, and can be installed with:

		$ pacman -S pyqt

#### Keyring ####

For *Ubuntu based* systems, Keyring is in the official repositories, and can be
installed the following way:

1. For Ubuntu (GNOME):

		$ sudo apt-get install python-keyring-gnome

1. For Kubuntu (KDE):

		$ sudo apt-get install python-keyring-kwallet

For *Arch Linux*, Keyring is in an AUR repository. If you have [yaourt] [yaourt],
you can install it with (if you don't have yaourt, you should really 
[get it] [yaourt]

		$ yaourt -S python-keyring

Other OS should read [Python Keyring installation docs] [keyring-install].

#### Twisted ####

For *Ubuntu based* systems, Twisted is in the official repositories, and can be
installed the following way:

*Ubuntu Lucid (10.04)*: the version included in the official repositories (10.0)
is older than what Pyfire requires. You can use twisted PPA's repository
instead, and install Twisted:

		$ sudo add-apt-repository ppa:twisted-dev/ppa
		$ sudo apt-get update
		$ sudo apt-get install python-twisted

*Ubuntu Maverick (10.10)*: the version included is what Pyfire requires, so
Twisted can be easily installed with:

		$ sudo apt-get install python-twisted

For *Arch Linux*, Twisted is in the extra repository and can be installed with:

		$ pacman -S twisted

Other OS should refer to the [Twisted download page] [twisted-download] which
shows how to install Twisted on several platforms. 

### Installing Snakefire ###

After all the required packages have been installed, you can install
Snakefire by:

1. Uncompressing the snakefire package file.
2. Unzip the downloaded file, and run the following command from within the 
created directory:

		$ python setup.py install

#### Running the developer version ####

If you wish to run the latest version of Snakefire, without having to
explicitly install it, follow these instructions:

1. Get the latest development version by cloning from its GIT repository:

		$ git clone git://github.com/mariano/snakefire

   You can keep up with the latest updates by accessing the directory where
   you installed Sakefire, and running:

		$ git pull --rebase && git submodule update --rebase

2. If you are on *KDE*, install the notify configuration to your home directory
   by running the following commands from the directory where you installed
   Sakefire:

		$ mkdir -p ~/.kde/share/apps/Snakefire
		$ cp *.png ~/.kde/share/apps/Snakefire
		$ cp *.notifyrc ~/.kde/share/apps/Snakefire
		$ killall knotify4

You are now ready to run Snakefire. Enter the directory where you installed
Snakefire, and do:

		$ python snakefire.py

[license]: http://www.opensource.org/licenses/mit-license.php
[pyfire-readme]: http://github.com/mariano/pyfire#readme
[yaourt]: http://wiki.archlinux.org/index.php/Yaourt
[keyring-install]: http://pypi.python.org/pypi/keyring/#installation-instructions
[twisted]: http://twistedmatrix.com
[twisted-download]: http://twistedmatrix.com/trac/wiki/Downloads