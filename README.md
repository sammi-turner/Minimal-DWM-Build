# Minimal-DWM-Build

A very minimal dwm set up to build from source

## By the way, I'm not using Arch

To install the pre-requisites in Ubuntu-based distros, enter the following command

```
sudo apt install libx11-dev libxft-dev libxinerama-dev lxappearance suckless-tools dmenu
```

## Build process

1. Clone or download this repo and cd into the folder.
2. Set permissions on 'DWM.desktop' and 'Makefile' to allow execution using either the command line or the right-click menu in your graphical file manager.
3. Change the owner of /usr/share/xsessions/ from root to the normal user with this command

```
sudo chown -R $USER
```
4. Copy the 'DWM.desktop' file to /usr/share/xessions/ with the command line or the right-click menu your graphical file manager.
5. Build dwm with this command

```
sudo make clean install
```
6. Log out of your session and when you log back in, select 'DWM Session' from the menu rather than your default file manager.

## Keybinds

I have hard-coded the following keybinds in config.h, which are listed in the 'cheat-sheet.txt' file in this repo. The config.def.h file shows the default settings for dwm.

```
MODIFIERS             KEY			                  FUNCTION

ALT                   d			                    run dmenu
ALT                   Space                     toggle tiled/floating layout
ALT			              Tab			                  toggle between current/last view

ALT                   Left mouse-click          move floating window
ALT                   Right mouse-click         resize floating window

ALT			              {1...9}		                switch to numbered view
ALT|SHIFT     	      {1...9}                   move window to numbered view

ALT                   v                         view all windows
ALT                   t                         tag all views with this window

ALT                   q			                    quit focused window
ALT                   m      		                move window from stack to master

ALT                   j			                    focus window clockwise
ALT                   k			                    focus window counterclockwise

ALT                   F9                        raise volume
ALT                   F10                       lower volume
ALT                   F11                       mute sound
ALT                   F12			                  quit session
```

## Changing your config.h

To change the default keybinds, change the default keybinds, recompile dwm, log out and back in.


