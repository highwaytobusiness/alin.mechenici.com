---
layout: page
title: Personal cheatsheet tl;dr;search
permalink: /cheatsheet/
---


About this page:

This one page cheatsheet is a (more) convenient way to store potential blog posts, interesting resources and technical experiences with the world. Before starting this I used different other platforms like [de.icio.us](https://del.icio.us/alin.mechenici), [twitter](https://twitter.com/alinmechenici), etc.

I encourange you to use the table of contents and Ctrl + f to find more easily.

# Table of Contents

My Linux Cheatsheet
- [My Linux Checklist](#my-linux-checklist)
- [Applications installed](#applications-installed)

My [dotfiles](http://alin.mechenici.com/dotfiles)

- [AwesomeWM](http://alin.mechenici.com/dotfiles#awesomewm)
- [i3WM](http://alin.mechenici.com/dotfiles#i3wm)
- [Emacs](http://alin.mechenici.com/dotfiles#emacs)
- [Mutt](http://alin.mechenici.com/dotfiles#mutt)
- [Zsh](http://alin.mechenici.com/dotfiles#Zsh)
- [bin scripts](http://alin.mechenici.com/dotfiles#bin-scripts)

My MacOS Cheatsheet

- [Article: "My MacOS apps & workflows"](http://alin.mechenici.com/macos)

My iOS Cheatsheet

- [Article: "iOS for webDev"](http://alin.mechenici.com/ios-webdev)
- [Article: "Affinity Photo (now) & Designer (later)"](http://alin.mechenici.com/affinity-for-ios)

Programs (external) Cheatsheet

- [Platforms](#platforms)
- [Programming Languages](#programming-languages)
- [Front-End Development](#front-end-development)
- [Back-End Development](#back-end-development)
- [Computer Science](#computer-science)
- [Big Data](#big-data)
- [Theory](#theory)
- [Books](#books)
- [Editors](#editors)
- [Tools](#tools)
- [Development Environment](#development-environment)
- [Entertainment](#entertainment)
- [Databases](#databases)
- [Media](#media)
- [Security](#security)
- [Content Management System](#content-management-system)
- [Project Management](#project-management)
- [Miscellaneous](#miscellaneous)
- [Browsers](#browsers)


Keyboard Shortcuts

- [Keyboard description](#keyboard-description)
- [Keyboard shortcuts automation](#keyboard-shortcuts-automation)

WebApps Shortcuts

- [Gmail](#gmail)
- [RemembertheMilk](#rememberthemilk)

Apps Shortcuts

- [Emacs shortcuts](#emacs-shortcuts)
- [Mutt shortcuts](#mutt-shortcuts)
- [VYM shortcuts](#vym-shortcuts)
- [Firefox shortcuts](#firefox-shortcuts)
- [Remember the Milk shortcuts](#remember-the-milk-shortcuts)

===============================================================

# My Linux Cheatsheet

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


#### search

    apt-cache search

#### SSH

    sysv-rc-conf

    /etc/init.d/ssh start

    /etc/init.d/sshd_config start/stop

### Mounded

    lsbsk - what is mounted

    dmesg -c = clear


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

# MPV

    - ls music

    - find

> stream > playlist (1)

    cat playlist 1

    find -type f (files) | grep -v pl[0-9]>playlist1

    mpv --playlist pl1


--------------------------------------------

# Programming Cheatsheet

## Platforms

- [Android-Cheatsheet-For-Graphic-Designers](http://petrnohejl.github.io/Android-Cheatsheet-For-Graphic-Designers/)
- [Arduino_Cheat_Sheet.pdf](https://static.sparkfun.com/learn/materials/8/Arduino_Cheat_Sheet.pdf)
- [docker](https://github.com/wsargent/docker-cheat-sheet)
    - [dockerfiles](https://github.com/jessfraz/dockerfiles)
- [ios-cheat-sheet](https://github.com/Avocarrot/ios-cheatsheet)
    - [iOS-App-Performance-Cheatsheet](https://github.com/danielamitay/iOS-App-Performance-Cheatsheet)
    - [UI-Testing-Cheat-Sheet](https://github.com/joemasilotti/UI-Testing-Cheat-Sheet)
- [saltstack](https://github.com/saltstack/salt/wiki/Cheat-Sheet)
- [nginx-cheatsheet](https://github.com/SimulatedGREG/nginx-cheatsheet)


## Programming Languages

- [Ada-cheat-sheet](http://www.digilife.be/quickreferences/QRC/Ada%20Reference%20Card.pdf)
- [assembly-cheat-sheet](http://www.jegerlehner.ch/intel/)
- [coffeescript_cheatsheet](https://github.com/icebob/coffeescript_cheatsheet/)
- [c-ansi-cheat-sheet](http://www.digilife.be/quickreferences/qrc/c%20reference%20card%20(ansi)%202.2.pdf)
- [c#-cheat-sheet ](http://www.digilife.be/quickreferences/QRC/Core%20CSharp%20and%20.NET%20Quick%20Reference.pdf)
- [cpp-cheat-sheet](https://isocpp.org/blog/2012/12/c11-a-cheat-sheet-alex-sinyakov)
- [clojure-cheat-sheet](https://clojure.org/cheatsheet)
- [clojurescript-cheat-sheet](http://cljs.info/cheatsheet/)
- [dart-cheat-sheet](http://dartlangfr.net/dart-cheat-sheet/)
- [delphi-cheat-sheet](http://www.cheat-sheets.org/saved-copy/dquick.pdf)
- [dotnet-cheat-sheet](https://dzone.com/refcardz/coredotnet)
- [elixir-cheat-sheet](https://media.pragprog.com/titles/elixir/ElixirCheat.pdf)
- [elm-cheat-sheet](https://github.com/izdi/elm-cheat-sheet)
- [erlang-cheat-sheet](http://www.cheat-sheets.org/saved-copy/Erlang.CheatSheet(1.0).pdf)
- [emoji-cheat-sheet](https://github.com/WebpageFX/emoji-cheat-sheet.com)
- [f#-cheat-sheet](http://dungpa.github.io/fsharp-cheatsheet)
- [golang-cheat-sheet](https://github.com/a8m/go-lang-cheat-sheet)
    - [Cheat sheet for some of the common concurrent flows in Go](https://github.com/rakyll/coop)
- [java-cheat-sheet](http://introcs.cs.princeton.edu/java/11cheatsheet/)
    - [java8-cheat-sheet](https://github.com/BafS/Java8-CheatSheet)
- [javascript-cheat-sheet](http://www.cheatography.com/davechild/cheat-sheets/javascript/)
    - [es6-cheatsheet](https://github.com/DrkSephy/es6-cheatsheet)
    - [javascript-design-pattern](https://github.com/nnupoor/js_designpatterns)
    - [npm-vs-yarn-cheat-sheet](https://shift.infinite.red/npm-vs-yarn-cheat-sheet-8755b092e5cc#.91l58dovs)
    - [npm-vs-yarn-cheat-sheet](https://github.com/areai51/yarn-cheatsheet)
- [lisp-cheat-sheet](http://faculty.smcm.edu/acjamieson/s13/LispCheatSheet.pdf)
- [lua-cheat-sheet](http://lua-users.org/files/wiki_insecure/users/thomasl/luarefv51single.pdf)
- [objective-c-cheat-sheet](https://github.com/iwasrobbed/Objective-C-CheatSheet)
- [ocaml-cheat-sheet](http://ocaml.org/docs/cheat_sheets.html)
- [python-cheat-sheet](http://www.cheatography.com/davechild/cheat-sheets/python/)
    - [Python Cheat Sheet](https://perso.limsi.fr/pointal/_media/python:cours:mementopython3-english.pdf)
    - [Python Cheat Sheet](https://docs.google.com/file/d/0B9VT_L2CDnKvODYyNTc5NjktYmMyOC00NDFkLTliNTctMzQzMTAzYjUyYmYy/view?pli=1)
    - [Python Crash Course - Cheat Sheets](http://ehmatthes.github.io/pcc/cheatsheets/README.html)
    - [python feature](https://github.com/PythonCharmers/python-future)
    - [Python Basics For Data Science Cheat Sheet](https://www.datacamp.com/community/tutorials/python-data-science-cheat-sheet-basics)
- [php-cheat-sheet](http://www.cheatography.com/davechild/cheat-sheets/php/)
    - [PHP7-Reference](https://github.com/tpunt/PHP7-Reference)
- [perlcheat](http://perldoc.perl.org/perlcheat.html)
- [r-cheat-sheet](http://cran.r-project.org/doc/contrib/Baggott-refcard-v2.pdf)
    - [R Cheat Sheets](https://www.rstudio.com/resources/cheatsheets/)
- [racket-cheat-sheet](http://docs.racket-lang.org/guide/)
- [ragel-cheat-sheet](https://github.com/calio/ragel-cheat-sheet)
- [rebol-cheat-sheet](http://rebol.desajn.net/cheatsheet.html)
- [ruby-cheat-sheet](https://github.com/brennovich/cheat-ruby-sheets)
    - [A collection of Ruby Net::HTTP examples](https://github.com/augustl/net-http-cheat-sheet)
- [rust-cheat-sheet](https://static.rust-lang.org/doc/0.9/complement-cheatsheet.html)
- [scala-cheat-sheet](http://docs.scala-lang.org/cheatsheets/)
- [scheme-cheat-sheet](http://courses.cs.washington.edu/courses/cse341/02wi/scheme/cheat-sheet.html)
- [shell-cheat-sheet](https://github.com/NisreenFarhoud/Bash-Cheatsheet)
    - [bash cheat sheet](https://learncodethehardway.org/unix/)
        - [awesome-bash](https://github.com/awesome-lists/awesome-bash)
        - [bash redirections](https://github.com/pkrumins/bash-redirections-cheat-sheet)
    - [fish](https://fishshell.com/docs/current/commands.html)
    - [awesome-shell](https://github.com/alebcay/awesome-shell)
    - [oh-my-zsh cheatsheet](https://github.com/robbyrussell/oh-my-zsh/wiki/Cheatsheet)
- [smalltalk-cheat-sheet](http://stephane.ducasse.free.fr/Teaching/0809Turino/st-cheatsheet.pdf)
- [swift cheatsheet](https://github.com/iwasrobbed/Swift-CheatSheet)
    - [Playgrounds](https://github.com/uraimo/Awesome-Swift-Playgrounds)
    - [swift design patterns](https://github.com/ochococo/Design-Patterns-In-Swift)
- [tcl-cheat-sheet](http://wiki.tcl.tk/10710)
- [typescript-cheat-sheet](http://www.typescriptlang.org/Handbook/)

## Front-End Development

- [angular2](https://angular.io/cheatsheet)
- [angularjs](http://www.cheatography.com/proloser/cheat-sheets/angularjs/)
- [SCSS cheatsheet](https://sass-cheatsheet.brunoscopelliti.com)
- [CSS Flex Box](https://d13yacurqjgara.cloudfront.net/users/248947/screenshots/1742074/attachments/282954/flexboxsheet.pdf)
- [sass/SCSS functions cheatsheet](https://gist.github.com/AllThingsSmitty/3bcc79da563df756be46)
- [ember-js](http://www.cheatography.com/mwore/cheat-sheets/ember-js/)
- [es6-cheatsheet](https://github.com/DrkSephy/es6-cheatsheet)
- [font-awesome](http://fontawesome.io/cheatsheet/)
- [jquery](https://oscarotero.com/jquery/)
    - [jquery-cheatsheet](http://lab.abhinayrathore.com/jquery-cheatsheet/)
- [react-cheatsheet](https://reactcheatsheet.com/)
- [react-native-cheat-sheet](https://github.com/refinery29/react-native-cheat-sheet)
- [react-native-styling-cheat-sheet](https://github.com/vhpoet/react-native-styling-cheat-sheet)
- [redux](http://ricostacruz.com/cheatsheets/redux.html)
- [underscore-cheat-sheet](http://f.cl.ly/items/093o0l2Y3u130y0W0c0x/underscore-cheat-sheet.pdf)
- [webpack](https://github.com/petehunt/webpack-howto)
- [\<head> Cheat Sheet](http://gethead.info/)
- [page-load Cheat Sheet](https://developers.google.com/speed/docs/insights/about)
- [Bootstrap 4](https://hackerthemes.com/bootstrap-cheatsheet/)
- [jest-cheat-sheet](https://github.com/sapegin/jest-cheat-sheet)
- [flexbox-cheatsheet](http://vudav.github.io/flexbox-cheatsheet/)

## Back-End Development

- [flask](https://docs.google.com/file/d/1pnwfq8v5Ph4Xn8ttv9P_TLnrRbT9-S_v-KdZiEcx64vlGYkC0SoMfZOs0NYN/edit?usp=drive_web)
- [laravel-cheatsheet](https://github.com/jesseobrien/laravel-cheatsheet)
- [ror](http://www.cheatography.com/davechild/cheat-sheets/ruby-on-rails/)
- [web2py](https://dl.dropboxusercontent.com/u/18065445/web2py/web2py_cheatsheet.pdf)
- [nodejs](https://gist.github.com/LeCoupa/985b82968d8285987dc3), [node api](https://nodejs.org/api/path.html)

- [ExpressJS API docs](http://expressjs.com/en/api.html)

- [django](http://awesome-django.com)
- [django-cheatsheet](https://www.mercurytide.co.uk/media/resources/django-cheat-sheet.pdf)
- [syscall-cheatsheet](http://syscalls.kernelgrok.com/)

## Big Data
- [machine-learning-cheat-sheet](https://github.com/soulmachine/machine-learning-cheat-sheet)

## Databases

- [CouchDB Cheatsheet](https://wiki.apache.org/couchdb/API_Cheatsheet)
- [MongoDb-cheat-sheet](https://github.com/leojavier/MongoDb-cheat-sheet)
- [mysql-cheat-sheet](http://www.cheatography.com/davechild/cheat-sheets/mysql/)
- [Oracle_Programming](https://en.wikibooks.org/wiki/Oracle_Programming/SQL_Cheatsheet)
- [postgresql](https://dzone.com/refcardz/essential-postgresql)
- [sql-join-cheat-sheet](http://coolshell.cn/articles/3463.html)
- [SQL](http://www.sql-tutorial.net/sql-cheat-sheet.pdf)
- Neo4j [manual for linux](https://neo4j.com/docs/operations-manual/current/installation/linux/), [linux install](https://neo4j.com/download-thanks/?edition=community&release=3.2.4&flavour=unix&_ga=2.260749903.35770474.1505387257-1130915347.1505387257), [stackoverflow tag](https://stackoverflow.com/questions/tagged/neo4j), [localhost](http://localhost:7474/browser/)

## Theory

- [acm-cheat-sheet](https://github.com/soulmachine/acm-cheat-sheet)
- [bigo](http://bigocheatsheet.com/)
- [Theoretical Computer Science Cheat Sheet](http://www.tug.org/texshowcase/cheat.pdf)
- [regular-expression-cheat-sheet](https://github.com/niklongstone/regular-expression-cheat-sheet)
- [rest-foundations-restful](https://dzone.com/refcardz/rest-foundations-restful)

## Editors

- [GNU Emacs](https://www.gnu.org/software/emacs/refcards/pdf/refcard.pdf)
    - [Paredit Cheatsheet](https://www.emacswiki.org/emacs/PareditCheatsheet)
- [MarkDown Cheat Sheet](https://guides.github.com/pdfs/markdown-cheatsheet-online.pdf)
- [Atom](https://github.com/nwinkler/atom-keyboard-shortcuts)
- [Sublime Text 3](https://www.shortcutfoo.com/app/dojos/sublime-text-3-win/cheatsheet)

## Tools

- [awk-nawk-and-gawk-cheat-sheet](http://www.catonmat.net/blog/awk-nawk-and-gawk-cheat-sheet/)
- [curl](https://github.com/bagder/curl-cheat-sheet)
- [dtrace and stap](http://myaut.github.io/dtrace-stap-book/dtrace-stap-cheatsheet.pdf)
- [GDAL/OGR command-line tools](https://github.com/dwtkns/gdal-cheat-sheet)
- [Git Cheat Sheet and Git Flow](https://github.com/arslanbilal/git-cheat-sheet)
    - [git_cheat_sheet](http://rogerdudler.github.io/git-guide/files/git_cheat_sheet.pdf)
    - [git-cheat-sheet](https://github.com/arslanbilal/git-cheat-sheet)
    - [github-cheat-sheet](https://github.com/tiimgreen/github-cheat-sheet)
    - [git-style-guide](https://github.com/agis/git-style-guide)
    - [git-flow-cheatsheet](https://github.com/danielkummer/git-flow-cheatsheet)
- [latexsheet](http://wch.github.io/latexsheet/)
- [mac-command-line-cheatsheet](https://github.com/herrbischoff/awesome-osx-command-line)
- [matlab-cheatsheet](http://web.mit.edu/18.06/www/Spring09/matlab-cheatsheet.pdf)
- [Octave-cheatsheet](http://ais.informatik.uni-freiburg.de/teaching/ss14/robotics/etc/cheatsheet.pdf)
- [rspec](https://gist.github.com/dnagir/663876)
- [RSpec cheatsheet](https://github.com/eliotsykes/rspec-rails-examples)
- [svn](http://www.abbeyworkshop.com/howto/misc/svn01/)
- [sed-stream-editor-cheat-sheet](http://www.catonmat.net/blog/sed-stream-editor-cheat-sheet/)
- [terminal-mac-cheatsheet](https://github.com/0nn0/terminal-mac-cheatsheet)
- [tmux](https://gist.github.com/andreyvit/2921703)
- [Unix Toolbox](http://cb.vu/unixtoolbox.xhtml)
- [sysadmin](https://github.com/kahun/awesome-sysadmin)
- [systemtap-cheat-sheet](https://github.com/calio/systemtap-cheat-sheet)

## Media

- [favicon-cheat-sheet](https://github.com/audreyr/favicon-cheat-sheet)

## Security

- [HTML5 Security Cheatsheet](https://github.com/cure53/H5SC)
- [Penetration Testing Cheatsheets](https://github.com/jshaw87/Cheatsheets)
- [Security Tools Cheatsheets](https://github.com/andrewjkerr/security-cheatsheets)
- [oauthsecurity](https://sakurity.com/oauth)
- [OWASP Cheat Sheets](https://www.owasp.org/images/9/9a/OWASP_Cheatsheets_Book.pdf)

## Project Management

- [Agile Cheatsheet](http://cheatsheetworld.com/programming/agile-development-cheat-sheet/)
- [Scrum Cheatsheet](https://www.axosoft.com/Downloads/Scrum_Diagram.pdf)
- [Lean Cheatsheet](https://www.cheatography.com/davidpol/cheat-sheets/lean-methodology/pdf_bw/)
- [A set of metodologies in one Cheatsheet (waterfall, agile, lean, xp, etc)](https://www.cheatography.com/nataliemoore/cheat-sheets/system-development-methodologies/pdf_bw/)

## Miscellaneous

- [easings.net](https://github.com/ai/easings.net)
- [math-as-code](https://github.com/Jam3/math-as-code)
- [MobileApp-Pentest-Cheatsheet](https://github.com/tanprathan/MobileApp-Pentest-Cheatsheet)
- [Network-related cheatsheets](http://packetlife.net/library/cheat-sheets/)
- [api-cheat-sheet](https://github.com/RestCheatSheet/api-cheat-sheet)
- [cheatsheets-ai](https://github.com/kailashahirwar/cheatsheets-ai)


## Browsers
- [Chrome keyboard shortcuts](https://support.google.com/chrome/answer/157179?hl=en)
- [Firefox keyboard shortcuts](https://support.mozilla.org/en-US/kb/keyboard-shortcuts-perform-firefox-tasks-quickly?redirectlocale=en-US&redirectslug=Keyboard+shortcuts)

=============================================


===========================================

Other Resources:

Idea for this page is taken from [smalldata.tech](https://smalldata.tech/cheatsheets) and some of the cheatsheets are based on: [Awesome Cheatsheet](https://github.com/detailyang/awesome-cheatsheet)
