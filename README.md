binhost-utils
=============
A utility for building and maintaining a binary package server for Gentoo Linux.

Binary packages in built inside chroot environments on a host machine, you can
create any number of environments with different settings.

Configuring the Environment(s)
------------------------------
An environment is created by extracting stage3 files into a sub-folder of the
chroots directory.

Inside the 'res/' directory are template files which get copied into the
environments, it is here you should set any settings such as CFLAGS and
USE Flags, subdirectories with the same name as an environment can contain
further files to override the default settings in 'res/'.

These files should be edited to match your environment as much as possible,
however FEATURES and DIST/PKGDIR settings in 'make.conf' should remain unchanged.
This also applies to all 'make.conf' files within environment subdirectories.

Quickstart
----------
	cd chroots/gentoo-amd64
	wget ftp://mirror.bytemark.co.uk/gentoo/releases/amd64/current-stage3/default/20130321/stage3-amd64-20130321.tar.bz2
	tar xvjpf stage3-*.tar.bz2
	cd ../..
	./binhost emptytree gentoo-amd64
	./binhost install gentoo-amd64 app-portage/gentoolkit

Installing and Updating Packages
----------------------------

Serving Packages to Hosts
-------------------------

Tips, Tricks and Troubleshooting
---------------------------------

License
-------
This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.
