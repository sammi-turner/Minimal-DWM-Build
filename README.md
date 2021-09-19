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
3. Change directory to

```
/usr/share/xsessions/ 
```

and switch ownership of that directory from root to the normal user by entering

```
sudo chown -R $USER
```

4. Copy the 'DWM.desktop' file to /usr/share/xessions/ with the command line or the right-click menu in your graphical file manager.
5. Build dwm with this command

```
sudo make clean install
```

6. Log out of your session.
7. When you log back in, select 'DWM Session' from the menu rather than your default desktop environment.

## Change themes and icons with lxappearance

The default gtk and icon themes are ugly, but they can easily be changed. Type 'lxappearance' into dmenu to launch a graphical tool to change your settings. Personally, I use the materia-dark-compact theme and the papirus-dark icons.

## Keybinds

I have hard-coded some keybinds in config.h, which are shown in the 'cheat-sheet.png' file. The 'config.def.h' file shows the default settings for dwm.

## Changing your config.h

To change the default keybinds, change the 'config.h' file, recompile dwm, log out, and then log back in.

## No clock, calendar or volume control?

Nah. I don't really need them.

If you want to run external scripts, then you might be better off starting with the [official default build](https://dwm.suckless.org/) and customising with patches from there.

## What about Snazzy Window Manager?

I am no longer maintaining that project, but there is still [a fork of it](https://github.com/Draco309/Snazzy-Window-Manager) on GitHub.
