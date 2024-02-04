
Debian
====================
This directory contains files used to package gaussaid/gaussai-qt
for Debian-based Linux systems. If you compile gaussaid/gaussai-qt yourself, there are some useful files here.

## gaussai: URI support ##


gaussai-qt.desktop  (Gnome / Open Desktop)
To install:

	sudo desktop-file-install gaussai-qt.desktop
	sudo update-desktop-database

If you build yourself, you will either need to modify the paths in
the .desktop file or copy or symlink your gaussai-qt binary to `/usr/bin`
and the `../../share/pixmaps/gaussai128.png` to `/usr/share/pixmaps`

gaussai-qt.protocol (KDE)

