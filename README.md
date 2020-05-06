# Installation


Edit config.mk to match your local setup (dmenu is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install dmenu
(if necessary as root):

   ``` make clean install ```


# Running dmenu

See the man page for details.

Usage: dmenu [OPTION]...

Display newline-separated input stdin as a menubar

```

-b                     show dmenu at the bottom
-h   N                 set dmenu to be N pixels high
-w   W                 set dmenu to be N pixels horizontally
-x   X                 set dmenu horizontal position
-y   Y                 set dmenu vertical position
-i                     dmenu matches menu items case insensitively
-l   L                 dmenu lists items vertically, within the
                       given number of lines
-m                     dmenu appears on the given Xinerama screen
-p  PROMPT             prompt to be displayed to the left of the
                       input field

-r,                    print out the current text each time a key is pressed
-si i                  preselected index after the menu opens


-fn FONT              font or font set to be used
-nb  COLOR            normal background color
                                  
-nf  COLOR            normal foreground color
-sb  COLOR            selected background color
-sf  COLOR            selected foreground color
-v                    display version information 
```

pango-imlib 
-------------
Thumbnails get cached according to XDG thumbnail spec.
http://specifications.freedesktop.org/thumbnail-spec/thumbnail-spec-latest.html

Pass -g to generate thumbnails immediatly for the piped images.
Pass -is to specify image size (keeping aspect ratio).
Pass -ia to specify image alignment (top-center/center/top/bottom/*-gapless, where top-center is default)
Note, that using too big images cause slowdown because images are loaded each time, selection image differs from last image.

Example pipe listing with images:
IMG:/mnt/pictures/lolcat.jpg\tThis is a lolcat\n
IMG:/mnt/pictures/david.jpg\tThis is a picture of david\n
This is a item without a picture\n

Additional options:
Pass -si to specify starting index to dmenu.
ex. -si 5 to start from item 5.
