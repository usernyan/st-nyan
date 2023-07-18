st - simple terminal
--------------------
st is a simple terminal emulator for X which sucks less.

## usernyan's changes
+ Scrollback with `shift-pageup/down` or `shift-scrollup/down`
+ Does _not_ cut off text on window resize
+ desktopentry patch, ads a desktop entry for st

### Visual stuff:
+ Use Xresources or pywal for dynamic colors/fonts
+ Transparency/alpha, adjustable from Xresources
+ Default font is "mono"
+ boxdraw patch, Box-drawing characters are rendered without gaps
+ font2 patch, have fallback fonts in config.h
+ anysize patch, the terminal window can adjust to any size, not just multiples of the char width/height

Requirements
------------
In order to build st you need the Xlib header files.


Installation
------------
Edit config.mk to match your local setup (st is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install st (if
necessary as root):

    make clean install


Running st
----------
If you did not install st with make clean install, you must compile
the st terminfo entry with the following command:

    tic -sx st.info

See the man page for additional details.

Credits
-------
Based on Aurélien APTEL <aurelien dot aptel at gmail dot com> bt source code.

