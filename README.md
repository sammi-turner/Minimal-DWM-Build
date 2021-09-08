# Minimal-DWM-Build

A very minimal [dwm](https://dwm.suckless.org/) set up to build from source.

## By the way, I use Arch

To install the dependencies in Arch-based distros, enter the following command

```
sudo pacman -S libx11, libxft, libxinerama lxappearance dmenu
```

To install the specific programs used in my set-up

```
sudo pacman -S firefox thunar xfce4-terminal xfce4-screenshooter
```

# By the way, I'm not using Arch

To install the dependencies in Ubuntu-based distros, enter the following command

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
6. Log out of your session and when you log back in, select 'DWM Session' from the menu rather than your default desktop environment.

## Change themes and icons with lxappearance

The default gtk and icon themes are ugly, but they can easily be changed. Type 'lxappearance' into dmenu to launch a graphical tool to change your settings. Personally, I use the materia-dark-compact theme and the papirus-dark icons. I have included an example screenshot.

## Keybinds

I have hard-coded some keybinds in config.h, which are shown in the 'cheat-sheet.png' file. The 'config.def.h' file shows the default settings for dwm.

## Changing your config.h

To change the default keybinds, change the 'config.h' file, recompile dwm, log out, and then log back in.
