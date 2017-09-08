---
layout: page
title: Cheatsheet
permalink: /cheatsheet/
---

A combination of potential blog posts, stackoverflow answers and experience. ** Ctrl + F ** to find. Inspired by [smalldata.tech](https://smalldata.tech/cheatsheets)


#### Personal Cheatsheet


# Window Managers

## Awesome

    startx

	install: apt-get install awesome

	chose_theme = "default-modified"

	~/.config/awesome/rc.lua

    awesome -k

& su apt install xev
& su apt install lxappearance
& su apt install i3lock
20170908141031

Notes:

* xev = keyboard pointer (x-event)


### FontAwesome

- [FontAwesome](https://github.com/FortAwesome/Font-Awesome/releases)

- [playerctl](https://github.com/acrisci/playerctl/releases)

- [mulimedia keys](https://faq.i3wm.org/question/3747/enabling-multimedia-keys/?answer=3759#post-id-3759)

- [Arc Firefox Theme](https://github.com/horst3180/arc-firefox-theme) & [Mozilla Addons](https://addons.mozilla.org/en-US/firefox/collections/horst3180/a/)

- [Arc Theme debian](https://software.opensuse.org/download.html?project=home%3AHorst3180&package=arc-theme)


## i3

    apt install i3

Favorite font

    font pango:System San Francisco Display 10

Start compton

    exec compton

Always open thunar window manager when i3 starts

    exec_always thunar # open window manager

Stop the terminal bell (can be placed in a script or in i3 config file)

    xset b off

#### key bindings

Print key = printscreen

    bindsym Print exec bash /home/alin/bin/alinscreencapture

S+Print = printscreen, open in a photo manipulation program, save.

    bindsym Shift+Print exec bash /home/alin/bin/alinscreencaptureandedit

Open a design app

    bindsym $mod+Shift+d exec bash /home/alin/bin/designer

Open telegram

    bindsym $mod+Shift+t exec bash /home/alin/bin/telegram

===============================================


### search

    apt-cache search

### SSH

    sysv-rc-conf

    /etc/init.d/ssh start

    /etc/init.d/sshd_config start/stop

### Mounded

    lsbsk - what is mounted

    dmesg -c = clear

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

Mutt settings for gmail


## Markdown

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


=============================================
# MPV

    - ls music

    - find

> stream > playlist (1)

    cat playlist 1

    find -type f (files) | grep -v pl[0-9]>playlist1

    mpv --playlist pl1


=============================================

# Emacs

## Intro

    C = Ctrl

    M = Meta key (alt/ mac key)

    RET - Return / Enter key

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

## Dictionary

C-h t = tutorial

C-h i = info manual

C-h k = (describe keyboard shortcut)

C-h a = Search documentation

C-h w <command> = shows shortcut

C-l = clear screen

C-d = delete-char

C-q or C-v = insert quoted

C-k = kill line

M-d = kill word

M-u = upcase-word

M-l = downcase-word

M-c = capitalize-word

M-\ = delete orizontal space

C-y = yank

M-y = yank-pop

xclip = mouse buffer

..............................................

## Important keys

F10 = Compilation

F3 = file

F1 = python print script print("{ " + str() + "}")

F2 = open link in browser at cursor

F3 = New

F4 = Open cursor position in Zeal

F5 = Timestamp

F6 = Undefined

F7 = Mail mode

F8 = Open Neotree

F9 = Undefined

F12 = Undefined

PrtScr = prinscreen

C-Page Up = sound +

C-Page Down = sound -

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


## Run a workflow in multi-windows

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


=============================================


## Keyboard shortcuts

### Basics

C-x C-f = Open file

C-x C-s = Save a file

C-x C-w = Save as

C-x s = Save all

C-x C-V = revert to file

M-x = revert buffer

C-x K = close window/buffer

C-x C-c = Close a file

M-j = focus

M-j space = re-organize

M-m = maximize

..............................................

### Text editing

C-_ = undo

C-Space = Begin selection

C-g = cancel selection

C-k = cut selection

C-k = cut line

C-y = paste

C-x r s /# = copy selection to numbered clipboard

C-x r i /# = paste from numbered clipboard
Delete = delete

C-d = Fwd delete

M-d = delete word

D-d = fwd delete word

C-w = kill/cut

C-y = yand/paste

M-x = replace-string RET

..............................................

### Cursor management

M-f/ M-b = Word forward / backward

C-a/C-e = Jump to beginning / end of the line

M+{/ M+} = Paragraph forward / backward

C-v/ M-v = Page forward / backward

M-</ M-> = Document forward / backward

M-C-a/ M+C-e = C Function forward / backward

C-arrow up - next paragraph up

C-arrow down - next paragraph down

C-home = move cursor up

C-end = move cursor bottom

..............................................

### Search

C-s = Incremental search

C-r = Incremental search reverse

M-C-s = regex incremental search

M-C-r = regex incremental search reverse

M+% = Interactive Search and Replace

M+X = goto-line	Goto Line Number

M-C+b (or esc C+B) = Previous Matching Bracket

M-C+f (or esc Ctrl+F) = Next Matching Bracket


..............................................

### Formating

M-q = Re-flow Paragraph

M-C+\ = Indent Selection

M-u = Uppercase Word

M-l = Lowercase Word

M-c = Capitalize Word

C-x, C-u = Uppercase Selection

C-x, C-l = Lowercase Selection

C-x,C-+/- = text size

..............................................

### Macros

C-x ( = start macro

C-x ) = end macro

C-x e = execute macro
    e = again

..............................................
### Undefined

C-' = Comment

C-; = search

..............................................

### Buffer & window management

C-x 2 = split orizontal

C-x 3 = split vertical

C-x o = other window

C-x 0 = get rid of other window

C-x 1 = get rid of other windows

M-o = window re-arange

C-x,k =	Close

C-x, b = Next Window

C-x, Ctrl+B = Choose Window

C-x, 1 = Maximize

C-x, 2 = Split Horizontal

C-x, 3 = Split Vertical

C-x, o = Switch Focus Between Windows

M+` = Activate Menu Bar

.............................................

### Navigation and search

M-g M-g = go to line
    (holt alt and press "g" twice)

A-g A-g = go to line

C-s = interactive search

C-r = interactive search backward

M-> = end of buffer

M-> = beginning of buffer

M-x = occur RET find lines

.............................................

### Move

C-e - end of line

C-a - beginning of line

C- <- - one word left

C- -> - one word right

C-space, move with arrow = move text selected

C-S, select with arrows = select text

C-S 1,2,3,4,5,6,7,8,9 = move application to tag

.............................................
### Cut-n-paste

C-space

Esc- <- = delete word

C-d = delete character

C-_ = undo

C-k = delete until end of line

C-y - yank from kill-ring

..............................................

## Package mode

### Packages installed

M-x / package-install

M-x .. erc / join debian = irc

M-x .. magit-mode = git


..............................................

## Other emacs shortcuts

* Settings:  ~/.emacs.d/init.el (initial-scratch-message)

* Shift + left or right arrows to select a region

* emacs Alt +W copy region into clipboard

* emacs Ctrl+W cut  region into clipboard

* emacs Ctrl+Y paste from clipboard into emacs terminal

* Shift+Insert  paste from clipboard

* Save buffer to file: C-x C-s

* Search text: C-s

* Search w/ regular expression: C-s-Alt

* Exit emacs: C-x C-c

* Buffer list: C-x C-b

* Buffer switch: C-x b

* Maximize S-M

* Fullscreen S-F

* Search C-x C-s

* Focus S-j

* Open C-x C-f

* Open Emacs C-F5 (*soon)

* Screen mngm S-Shift-Space

* Undo C-Shift +

=============================================

=============================================

## VYM

View your Mind

### Scope Heading Editor:

- Ctrl+Shift+P: Superscript

- Ctrl+Shift+B: Subscript

- Ctrl+U: Underline

- Ctrl+I: Italic

- Ctrl+B: Bold

- Alt+R: Richtext

- Alt+I: Font hint

- Ctrl+V: Paste

- Ctrl+X: Cut

- Ctrl+C: Copy

- Ctrl+A: Select and copy all

- Ctrl+Y: Redo

- Ctrl+Z: Undo

- Ctrl+P: Print

- Alt+X: Export As(ASCII)

- Ctrl+S: Export

- Ctrl+O: Import

### Scope Main window:

- F: Follow XLink

- L: Use modifier to draw xLinks

- K: Use modifier to color branches

- J: Use modifier to color branches

- Backspace: Previous slide

- Space: Next slide

- Shift+Left: Previous Map

- Shift+Right: Next Map

- Ctrl+H: History Window

- Alt+S: Script editor

- Shift+S: Slide editor

- Q: Task editor

- Ctrl+T: Tree editor

- E: Heading editor

- N: Note editor

- .: Center on selection

- ,: reset Zoom

- R: Rotate rclockwise

- Shift+R: Rotate counterclockwise

- -: Zoom out

- +: Zoom in

- : Color subtree

- : Color branch

- Ctrl+K: Pick color

- : Set Color

- Shift+F: Find duplicate URLs

- /: Find

- Ctrl+F: Find

- : Unselect all

- Ctrl+I: Select next

- Ctrl+O: Select previous

- M: Move to target

- G: Goto target

- Shift+T: Toggle target

- P: Property window

- Shift+I: Add

- T: Add timestamp

- Shift+X: Remove children

- W: Cycle task status

- Shift+W: Toggle task

- Ctrl+B: Get data from SUSE Bugzilla for subtree

- Shift+B: Get data from SUSE Bugzilla

- B: Create URL to SUSE Bugzilla

- Alt+U: Use heading for URL

- : Edit local URL

- U: Edit URL

- Shift+N: Extract URLs from note
  - : Open all URLs in subtree
  - Ctrl+U: Open all URLs in subtree (including scrolled branches)

- : Open URL in new tab

- Shift+U: Open URL

-Ctrl+0: Reset selection size

- Ctrl+-: Shrink selection

- Ctrl++: Grow selection

- <: Collapse unselected levels

- Ctrl+<: Collapse one level

-  >: Expand one level

-  S: Scroll branch

-  Shift+O: Sort children backwards

- O: Sort children

- D: Detach

- PgDown: Move down

- PgUp: Move up

- Ctrl+A: Add branch below

- Ctrl+Ins: Add branch below

- Shift+A: Add branch above

- Shift+Ins: Add branch above

- Alt+A: Add branch (insert)

- A: Add branch as child

- C: Add mapcenter

- Del: Delete Selection

- Ctrl+V: Paste

- Ctrl+X: Cut

- Ctrl+C: Copy

- Ctrl+Y: Redo

- Ctrl+Z: Undo

- Ctrl+Q: Exit VYM

- Ctrl+W: Close Map

- Ctrl+P: Print

- Alt+E: Repeat last export (-)

- : Save

- Alt+R: Restore last session

- Ctrl+L: Open

- Ctrl+Shift+N: Copy to new map

- Ctrl+N: New map

### Scope Note Editor:

- Ctrl+Shift+P: Superscript

- Ctrl+Shift+B: Subscript

- Ctrl+U: Underline

- Ctrl+I: Italic

- Ctrl+B: Bold

- Alt+R: Richtext

- Alt+I: Font hint

- Ctrl+V: Paste

- Ctrl+X: Cut

- Ctrl+C: Copy

- Ctrl+A: Select and copy all

- Ctrl+Y: Redo

- Ctrl+Z: Undo

- Ctrl+P: Print

- Alt+X: Export As(ASCII)

- Ctrl+S: Export

- Ctrl+O: Import

## Want to learn

### Learn inskape

#### make vectorial from pictures

Open image (C-i) / (S+A+b) scans 2

## Firefox

# Keyboard shortcuts ([link](https://support.mozilla.org/en-US/kb/keyboard-shortcuts-perform-firefox-tasks-quickly?redirectlocale=en-US&as=u&redirectslug=Keyboard+shortcuts&utm_source=inproduct))

- C+t: new tab

- C+n: new window

- C+k: focus search bar

- C+Shift+v: paste in plain text

- C+w: close tab

- C+Shift+p: new private tab

- C+Shift+t undo close tab

- C+Shift+n undo closed window

- C+1 to 8: select tab 1 to 8

- C+Shift+Y: downloads

- C+h: history

- C+b: bookmarks

- C+Shift+0: library window (bookmarks)

- C+Shift+h: history window

- C+Shift+a: addons

- C+Shift+m: multipanel

- C+Shift+p: page info

- F4: close sidebar

- C+Shift+F4: AllinOneSidebar options

- C+Shift+k: web console

- Shift+F2: developer toolbar

- Shift+J: browser console

- Shift+F5: profiler

- Shift+F4: Scratchpad

- C+u: page source



## Kupfer

### Keyboard shortcuts

- S+Space: start

- A+a: alternate activate

- C+,: comma trick

- C+RET: compose command

- C+r: reset all

- C+q: select quit

- C+g: select selected file

- F1: show help

- C+;: show prefferences

- C+s: switch to first pane


===========================================


Resources:

- template [slides](https://github.com/highwaytobusiness/alin.mechenici.com/tree/gh-pages/slides)

