
Debian
====================
This directory contains files used to package dividendcashd/dividendcash-qt
for Debian-based Linux systems. If you compile dividendcashd/dividendcash-qt yourself, there are some useful files here.

## dividendcash: URI support ##


dividendcash-qt.desktop  (Gnome / Open Desktop)
To install:

	sudo desktop-file-install dividendcash-qt.desktop
	sudo update-desktop-database

If you build yourself, you will either need to modify the paths in
the .desktop file or copy or symlink your dividendcashqt binary to `/usr/bin`
and the `../../share/pixmaps/dividendcash128.png` to `/usr/share/pixmaps`

dividendcash-qt.protocol (KDE)

