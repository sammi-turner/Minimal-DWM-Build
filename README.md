# Minimal-DWM-Build

A very minimal [dwm](https://dwm.suckless.org/) set up to build from source.

## By the way, I use Arch

To install the dependencies in Arch-based distros, enter the following

```
sudo pacman -S libx11 libxft libxinerama lxappearance dmenu firefox
```

## By the way, I'm not using Arch

To install the dependencies in Ubuntu-based distros, enter the following

```
sudo apt install libx11-dev libxft-dev libxinerama-dev lxappearance suckless-tools dmenu firefox
```

## Build process if you ALREADY have the xfce4 desktop environment installed on your system

1. Clone or download this repo and cd into the folder.
2. Set permissions on 'DWM.desktop' and 'Makefile' to allow execution using either the command line or the right-click menu in your graphical file manager.
3. Enter the command

```
sudo chown -R $USER /usr/share/xsessions/
```

4. Copy the 'DWM.desktop' file to /usr/share/xessions/ with the command line or the right-click menu in your graphical file manager.
5. Build dwm with this command

```
sudo make clean install
```

6. Log out of your session.
7. When you log back in, select 'DWM Session' from the menu rather than your default desktop environment.

## Change themes and icons with lxappearance

The default gtk and icon themes are ugly, but they can easily be changed. 

Type 'lxappearance' into dmenu to launch a graphical tool to change your GTK theme and icons.

## Keybinds

I have hard-coded some keybinds in config.h. The 'config.def.h' file shows the default settings.

## Changing your config.h

To change the default keybinds, change the 'config.h' file, recompile dwm, log out, and then log back in.
