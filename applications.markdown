---
layout: page
title: Applications
permalink: /applications/
---

## Linux applications:

Prerequisites needs to be installed:

You can use the bulk install:

sudo apt install \

     bc \
     apt-transport-https \
     ca-certificates \
     curl \
     gnupg2 \
     software-properties-common \
     zsh \
     wget \
     python3 \
     tar \
     git \

Applications installed from the terminal.

You can use the bulk install:

    su RET pswd

apt install

    xev \
    lxappearance \
    i3lock \
    xclip \
    zeal \
    chromium \
    firefox \
    planner \
    terminator \
    gnome-alsamixer \
    mpv \
    dropbox \
    docker \
    dia \
    vym \
    gnome-calendar \
    gnome-commander \
    gnome-documents \
    gtranslator \
    ipython \
    keepass2 \
    inkscape \
    geeqie \
    calibre \

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


=============================================