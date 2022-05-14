# Minimal-DWM-Build

A very minimal [dwm](https://dwm.suckless.org/) set up to build from source.

## By the way, I use Arch

To install the dependencies in Arch-based distros, enter the following

```
sudo pacman -S libx11 libxft libxinerama lxappearance dmenu termite firefox nitrogen picom
```

## Cheat sheet

The default keybinds are listed in 'keybinds.txt'.

## Build process if you ALREADY have the xfce4 desktop environment installed on your system

1. Clone or download this repo and cd into the folder.
2. Set permissions on 'DWM.desktop' and 'Makefile' to allow execution using either the command line or the right-click menu in your graphical file manager.
3. Enter the commands

```
sudo chown -R $USER /usr/share/xsessions/
```

4. Copy the 'DWM.desktop' file to

```
/usr/share/xessions/ 
```

with the command line or the right-click menu in your graphical file manager.

5. Mark the 'dwm.session' file AS EXECUTABLE using either the command line or a graphical file manager.

6. Log in as the root user with the 'su' command, then copy the 'dwm.session' file to

```
/usr/local/bin/ 
```

7. As the normal user, build dwm with this command

```
sudo make clean install
```

8. Log out of your session.
9. When you log back in, select 'DWM Session' from the menu rather than your default desktop environment.

## Set the desktop background with Nitrogen.

On your first log in, the bar will appear, but not your desktop background!

So for your next log in, set your wallpaper using nitrogen.

## Change themes and icons with lxappearance

The default gtk and icon themes are ugly, but they can easily be changed. 

Type 'lxappearance' into dmenu to launch a graphical tool to change your GTK theme and icons.

## Keybinds

I have hard-coded my default keybinds in config.h. The 'config.def.h' file shows the default settings.

## Changing your config.h

To change the default keybinds, change the 'config.h' file, recompile dwm, log out, and then log back in.
