---
layout: page
title: Applications
permalink: /applications/
---

## Linux applications:

Prerequisites needs to be installed:

You can use the bulk install:

	sudo apt install \

	gdisk btrfs-tools git apache2 python-requests libapache2-mod-php python-pymssql build-essential python-pexpect python-pefile python-crypto python-openssl bc apt-transport-https ca-certificates curl gnupg2 software-properties-common zsh wget python3 tar i3lock curl build-essentials emacs xterm awesome xinit xserver-xorg alsa-utils sysv-rc-conf audacity ffmpeg mosh wicd-curses vorvis-tools libncurses-dev open-ssh-server mutt xev lxappearance i3lock xclip zeal chromium firefox-esr planner terminator gnome-alsamixer mpv dropbox docker dia vym gnome-calendar gnome-commander gnome-documents gtranslator ipython keepass2 inkscape geeqie calibre unrar network-manager-gnome lxpannel goldendict shutter simplescreenrecorder dia freecad pdf2svg gnome-music gnome-photos amarok digikam gthumb orage p7zip-full vorbis-tools alien pylint python3-pip pylint epc jedi virtualenv 	

	
Python install:

	pip3 install rainbowstream

	apt-get install python-dev libjpeg-dev libfreetype6 libfreetype6-dev zlib1g-dev
	
	pip install rope
	pip install jedi
	pip install flake8
	pip install importmagic



Use this command to install Node.js and npm

    curl -sL https://deb.nodesource.com/setup_6.x | sudo bash -
    sudo apt install nodejs npm

Install libreoffice without UI:

	apt-get --no-install-recommends install libreoffice

Other apps and plugins:

- [FontAwesome](https://github.com/FortAwesome/Font-Awesome/releases)

- [playerctl](https://github.com/acrisci/playerctl/releases)

- [mulimedia keys](https://faq.i3wm.org/question/3747/enabling-multimedia-keys/?answer=3759#post-id-3759)

- [Arc Firefox Theme](https://github.com/horst3180/arc-firefox-theme) & [Mozilla Addons](https://addons.mozilla.org/en-US/firefox/collections/horst3180/a/)

- [Arc Theme debian](https://software.opensuse.org/download.html?project=home%3AHorst3180&package=arc-theme)


Applications like: postman, noodl, onlyoffice, telegram, Remember The Milk, Gravit, skype, etc, to start from terminal / S-r

Example: Postman

     wget https://dl.pstmn.io/download/latest/linux64 -O postman.tar.gz
     sudo tar -xzf postman.tar.gz -C /opt
     rm postman.tar.gz
     sudo ln -s /opt/Postman/Postman /usr/bin/postman


More complex installations:

## [f.lux](https://justgetflux.com/linux.html)

Install dependencies:

	sudo apt-get install git python-appindicator python-xdg python-pexpect python-gconf python-gtk2 python-glade2 libxxf86vm1

Download [xflux-gui](https://github.com/xflux-gui/xflux-gui)

	 cd /tmp
	 git clone "https://github.com/xflux-gui/xflux-gui.git"
	 cd xflux-gui
	 python download-xflux.py

EITHER install globally

       sudo python setup.py install

EXCLUSIVE OR, install in your home directory. The binary installs
into ~/.local/bin, so be sure to add that to your PATH if installing locally.

     python setup.py install --user

Run flux

    fluxgui


Notes:

* xev = keyboard pointer (x-event)

* lxappearance = change the appearance in awesome and i3

* i3lock = lock the screen in awesome and i3

* flux = change to the night mode

* tar unpack = tar xvf file.tar

===============================================



## Neo4j

The Debian package is available from http://debian.neo4j.org. To use the repository follow these steps:

    wget -O - https://debian.neo4j.org/neotechnology.gpg.key | sudo apt-key add -
    echo 'deb http://debian.neo4j.org/repo stable/' | sudo tee -a /etc/apt/sources.list.d/neo4j.list
    sudo apt-get update

To install Neo4j Community Edition:

   sudo apt-get install neo4j=3.2.3

   apt-get install neo4j=3.2.4

Start:

	service neo4j start

Make defaul homepage in chromium:

     http://localhost:7474/browser/

=============================================

Keybase [linux](https://keybase.io/docs/the_app/install_linux)

	curl -O https://prerelease.keybase.io/keybase_amd64.deb
	# if you see an error about missing `libappindicator1`
	# from the next command, you can ignore it, as the
	# subsequent command corrects it
	sudo dpkg -i keybase_amd64.deb
	sudo apt-get install -f
	run_keybase


# MPV

    - ls music

    - find

> stream > playlist (1)

    cat playlist 1

    find -type f (files) | grep -v pl[0-9]>playlist1

    mpv --playlist pl1



# Docker

[docker install](https://docs.docker.com/engine/installation/linux/docker-ce/debian/#install-using-the-repository)


	install -y apt-transport-https ca-certificates wget software-properties-common

	wget https://download.docker.com/linux/debian/gpg
	su apt-key add gpg
	echo "deb [arch=amd64] https://download.docker.com/linux/debian $(lsb_release -cs) stable" | sudo tee -a /etc/sources.list.d/docker.list
	apt - cache policy docker-ce
	apt-get -y install docker-ce

Start:

	systemctl start docker
	systemctl stop docker
	systemctl restart docker
	systemctl status docker
	systemctl enable docker

/ verify installation

	docker run hello-world

/ allow not-root user to run docker

	sudo groupadd docker
	sudo useradd alin
	sudo usermod -aG docker alin
	
	docker run hello-world
	docker images
	docker run -i -t dadjada /bin/bash
	docker ps

Docker with gui

        curl -fsSL https://get.docker.com/ | sh
	sudo service docker start
	xauth list
	sudo docker run -i -t --net=host -e DISPLAY -v /tmp/.X11-unix ubuntu bash

Inside container:

       $ apt-get install firefox
       $ apt-get install xauth
       $ xauth add ...


# Virtualbox

emacs	/etc/apt/sources.list.d/virtualbox.list

	deb http://download.virtualbox.org/virtualbox/debian stretch contrib

public key:

	wget -q https://www.virtualbox.org/download/oracle_vbox_2016.asc -O- | apt-key add -

Install:

	apt update && apt install virtualbox-5.1

Start:

	virtualbox

[Documentation](https://www.virtualbox.org/wiki/End-user_documentation)

=============================================


chromium
chrome://extensions/configureCommands



