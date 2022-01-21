﻿# emacs_customization

copied from http://gewhere.github.io/orgmode-emacs-init-file

How to setup your Emacs init file using orgmode
A recommended way to setup your Emacs init file is to load it as an orgmode file. 
I am using Emacs Prelude, and it is not recommended to edit your ~/.emacs.d/init.el. 
In prelude the initialization files go into ~/.emacs.d/personal/preload/ folder.

In order to write your init.el as an orgmode file using Emacs Prelude do the following steps:

Step 1
- Make a file ~/emacs.d/personal/emacs-init.el with the content:

`code`

(require 'org)
(org-babel-load-file
 (expand-file-name "init.org"
                   /path/to/init.org))
                   
Step 2
- Make your orgmode init file in your custom path /path/to/init.org
- Your init.org should be like this:

`code`

* Personal info
#+BEGIN_SRC emacs-lisp
(setq user-full-name "Georgios Diapoulis")
#+END_SRC
* Keybindings
#+BEGIN_SRC emacs-lisp
(global-set-key (kbd "C-c h w") 'whitespace-mode)
(global-set-key (kbd "C-c h l") 'visual-line-mode)
#+END_SRC
Step 3
Restart Emacs
