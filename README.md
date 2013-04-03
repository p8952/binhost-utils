binhost-utils
=============

binhost-utils are a set of utilities for building and maintaining a binary 
package server on/for Gentoo Linux.

Binary packages in built inside chroot environments on a host machine, you can
create any number of environments with different settings.

Configuring the Environment(s)
------------------------------

An environment is created by extracting the stage3 files into a sub-folder
of the chroots directory.

Inside the 'res/' directory are template files which get copied into the
environments, it is here you should set any settings such as CFLAGS and 
USE Flags, subdirectories with the same name as an environment can contain 
further files to override the default settings in 'res/'.

These files should be edited to match your environment as much as possible,
however FEATURES and PKGDIR settings in 'make.conf' should remain the same. 
This also applies to all 'make.conf' files within environment subdirectories.

Quickstart
----------

Installing/Updating Packages
----------------------------

Serving Packages to Hosts
-------------------------
