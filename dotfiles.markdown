---
layout: page
title: Dotfiles
permalink: /dotfiles/
---


# My dotfiles

Window Managers: AwesomeWM & i3

## AwesomeWM

    startx

	install: apt-get install awesome

	chose_theme = "default-modified"

	~/.config/awesome/rc.lua

    awesome -k

Awesome tags:

	1: start
	2: code
	3: internet
	4: idea
	5: agile
	6: office
	7: irc
	8: root
	9: other

Open apps at startup using:

     awful.util.spawn("emacs")

Open Applications in ONLY this specific tag:

1. free to open any app

2. code

- terminal split vertically in two (top)
- emacs (bottom)
- zeal (right)

3. chromium in incognito

4. VYM

5. Emacs in agile-mode

6. libreoffice, planner, calendar, gnome-commander, nautilus, documents, dictionary, zotero, etc

7. telegram, mutt, slack, irc, shared calendar, dropbox cli, twitter

8. terminal in root mode

9. mpv, etc



## i3WM

    apt install i3

Favorite font

    font pango:System San Francisco Display 10

Start compton

    exec compton

Always open thunar window manager when i3 starts

    exec_always thunar # open window manager



Key bindings

Print key = printscreen

    bindsym Print exec bash /home/alin/bin/alinscreencapture

S+Print = printscreen, open in a photo manipulation program, save.

    bindsym Shift+Print exec bash /home/alin/bin/alinscreencaptureandedit

Open a design app

    bindsym $mod+Shift+d exec bash /home/alin/bin/designer

Open telegram

    bindsym $mod+Shift+t exec bash /home/alin/bin/telegram



## Mutt

Mutt settings for icloud email ([*](https://forums.freebsd.org/threads/44264/))

    set imap_user = "user"
    set from = "user@icloud.com"
    set smtp_url = "smtp://user@smtp.mail.me.com:587/"

    set folder = "imaps://user@imap.mail.me.com/"
    set spoolfile = "imaps://user@imap.mail.me.com/INBOX"
    set postponed = "+Drafts"
    set record = "+Sent Messages"

    set imap_pipeline_depth=0

    set header_cache = "~/.mutt/cache/headers"
    set message_cachedir = "~/.mutt/cache/bodies"
    set certificate_file = "~/.mutt/certificates"



# Emacs

Useful terminal commands for working with emacs:

    emacs -nw = new emacs window

    watch tree = watch tree in terminal for 3 min

## Tricks

C-x C-q (cont..)

C-x C-s =  edit files and folders as a file

A-/ auto-complete cycle


## emacs checklist:

- medium, jekyll
- erc
- mutt
- slack
- excel
- notes / remember
- calendar gcal.el
- codepad
- ipython
- python compiler
- neotree
- google maps
- google translate
- google here *search
- eshell
- hackernews
- battery (laptop)
- dashboard
- bookmarks
- trump (webdav, ssh, )
- dropbox
- email
- telegram
- firefox-mode
- playerctl
- alin_modes
- emacs wm
- templates
- web server (w/ broweser sync)
- sync content with mobile and ipad via calendar and dropbox/mega/box
- excel updates
- artist mode
- org-mind-map
- github
- emmet mode (always on)

..............................................

IDEAS to implement:
- emacs + google calendar:

emacs files:

- notes.md (dropbox.el)
- TODO.md (dropbox.el)
- Doing.md (dropbox.el in sync with gcal.el)
- Done (sync with dropbox.el)
* all 4 sinced with trello


.............................................

## Compilation example

    emacs compile python ~/py/working/src/app.py

    M-x compile (enter)

	python ~/py/working/src/app.py

.............................................

# Emacs config and other daemons

## Theme and settings

    ; setup theme
    (load-theme 'misterioso) ; 'tango-dark


    ; remove menu, tab and scroll
    (menu-bar-mode -1)
    (tool-bar-mode -1)
    (scroll-bar-mode 0)

    ;text increasing
    (text-scale-adjust 1)


    ; start emacs in fullscreen mode
    (add-hook 'emacs-startup-hook 'toggle-frame-maximized)


    ; open browser where the cursor is
    (defun webbrowser-visit-thing-at-point()
        (interactive)
    (start-process "emacs-webbrowser-visit-thing-at-point-process" "*Messages*" "/home/rider/.emacs.d/x/webbrowserwrapper" (thing-at-point 'url)))
    (global-set-key [f2] 'webbrowser-visit-thing-at-point)

    ; use left, right arrows to visit another frame
    (global-set-key (kbd "C-c <left>") 'previous-multiframe-window)
    (global-set-key (kbd "C-c <right>") 'next-multiframe-window)


### codepad.org integration

    (add-to-list 'load-path ".emacs.d/roaming/codepad.el") ;; replace PATH with the path to codepad.el
    (autoload 'codepad-paste-region "codepad" "Paste region to codepad.org." t)
    (autoload 'codepad-paste-buffer "codepad" "Paste buffer to codepad.org." t)
    (autoload 'codepad-fetch-code "codepad" "Fetch code from codepad.org." t)



## Run a workflow in multi-windows

// Mx- RET notes



   (defun notes()
   	   (interactive)
	   ;(find-file "book.md")
	   (find-file "/home/alin/.emacs.d/notes")
	   (split-window-right)
	   (find-file "/home/alin/Work/TODO.md")

	   ;(find-file "/home/alin/.config/awesome/rc.lua")
	   ;  (split-window-right)
	   ;  (split-filet "/home/alin/work/README.md")
	   ;(split-window-right)
	   ;(find-file "/home/alin/.emacs.d/init.el")
	   ;(split-window-right)


	   ;(find-file "/home/alin/work/start.m")
	   (balance-windows))


Call "notes": f2


     (defun file-notes()
     	    (interactive)
  	    (find-file (concat (getenv "HOME") "/.emacs.d/notes")))
	    (global-set-key [f3] 'file-notes)
	    (global-set-key (kbd "<XF86Search>") 'file-notes)
	    (global-set-key (kbd "<XF86AudioRaiseVolume>") 'file-notes)



// M-x RET alin_start


    (defun alin_start()
        (interactive)

    ;(find-file "book.md")
    (find-file "/home/user/.emacs.d/init.el")
    (split-window-right)
    (find-file "/home/alin/work/planning/TODO.md")
    ;  (split-window-right)
    ;  (split-filet "/home/alin/work/README.md")
    (split-window-right)
    (find-file "/home/alin/work/now.py")
    (split-window-right)
    (find-file "/home/alin/work/start.md")
    (balance-windows))
    ;(add-hook 'emacs-startup-hook 'alin_start)

    ;(add-hook 'text-mode-hook 'auto-fill-mode)

* change files path with your own

## Dash-at-point (Zeal integration)
Use Zeal app with XF86WebCam (f8) key to open "zeal-at-point"

    ;(global-set-key "bla" 'zeal-at-point)
    (global-set-key [f1] 'zeal-at-point)
    (global-linum-mode t)

    ;; Use multiple docsets
    ;(add-to-list 'zeal-at-point-mode-alist '(python-mode . ("python" "django")))


## Neotree


    (add-to-list 'load-path "~/.emacs.d/neotree")
        (require 'neotree)
    (global-set-key [f8] 'neotree-toggle)

    (setq misterioso (if (display-graphic-p) 'icons 'arrow)) ; neo-theme


----------------------------

## OrgMode

Add tasks in OrgMode

* A-Return = *

** A- -> = sub-bullets

* A-arows up/down = Move

* TODO S- -> = To Do

* DONE S- <- = Done

### Checkbox [1/2]

    "["/"]" C-c, C-c adds number of items in checklist

  "["%"]" C-c, C-c adds procentage

- [ ] checkbox

- [X] checkbox checked (C-c, C-c)

- [ ] checkbox 3

### Deadlines

C-c C-d = Add deadlines

* go home

DEADLINE: <2017-07-16 Sun>

### Tags

C-c C-c = Add tags

### Hides

    Cursor tab = hide

    S-tab = hide more

### Save

    C-x C-s = save

### Agenda view

Start agenda view C-c [

A-x org-agenda

C-0 = back to original file

q = exit screen

* case sensitive ("m" for all or "M" for TODO)



C-h t = tutorial




## Configurations

Stop the terminal bell:

Can be placed in a script or in i3 config file:

    xset b off


Configure git:

	  git config --global user.name "Alin Mechenici"
	  git config --global user.email "alin at my email dot smth"

Create a new repository:


       git clone git@github.com:alinmechenici/somerepo.git
       cd repo
       touch README.md
       git add README.md
       git commit -m "add README"
       git push -u origin master

Existing folder: cd existing_folder

	 git init
	 git remote add origin git@github.com:alinmechenici/somerepo.git
	 git add .
	 git commit -m "Initial commit"
	 git push -u origin master

Existing Git repository

	 cd existing_repo
	 git remote add origin git@gitlab.com:alinmechenici/repo.git
	 git push -u origin --all
	 git push -u origin --tags
