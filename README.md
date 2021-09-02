# Minimal-DWM-Build

A very minimal dwm set up to build from source.

## By the way, I'm not using Arch

To install the pre-requisites in Ubuntu-based distros, enter the following command

```
sudo apt install libx11-dev libxft-dev libxinerama-dev lxappearance suckless-tools dmenu
```

To install the specific programs used in my set-up

```
sudo apt install firefox thunar xfce4-terminal xfce4-screenshooter 
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

## Change themes and icons with Lxappearance

The default gtk and icon themes are awful, but can easily be changed. Type in 'lxappearance' into dmenu to launch a graphical tool to change your settings. Personally, I use the materia-dark-compact theme and the papirus-dark icons. See the screenshot included in this repo.

## Cheat sheet

I have hard-coded some keybinds in config.h, which are listed in the 'cheat-sheet.png' file in this repo. The config.def.h file shows the default settings for dwm.

## Changing your config.h

To change the default keybinds, change the default keybinds, recompile dwm, log out and back in.
