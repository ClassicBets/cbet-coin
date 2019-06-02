
Debian
====================
This directory contains files used to package classicbetsd/classicbets-qt
for Debian-based Linux systems. If you compile classicbetsd/classicbets-qt yourself, there are some useful files here.

## classicbets: URI support ##


classicbets-qt.desktop  (Gnome / Open Desktop)
To install:

	sudo desktop-file-install classicbets-qt.desktop
	sudo update-desktop-database

If you build yourself, you will either need to modify the paths in
the .desktop file or copy or symlink your classicbetsqt binary to `/usr/bin`
and the `../../share/pixmaps/classicbets128.png` to `/usr/share/pixmaps`

classicbets-qt.protocol (KDE)

