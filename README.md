Kinum - The KDE Internet Usage Meter

DETAILS
=======

Initially intended as the KDE Internode Usage meter, Kinum will
serve as a pluggable popup applet/plasmoid that can support multiple
backends for different internet service provides (for example 
Internode, iiNet, etc.)

AUTHORS
=======

Terry Moschou <tmoschou@gmail.com>

BUILD INSTRUCTIONS
==================

git clone https://github.com/tmoschou/kinum.git
cd kinum
mkdir build
cd build
cmake -DCMAKE_INSTALL_PREFIX="$(kde4-config --prefix)" ..
(or
cmake -DCMAKE_INSTALL_PREFIX=~/.kde ..
)
make 
make install

Restart plasma to load the applet 
kquitapp plasma-desktop
plasma-desktop

or view it with 
plasmoidviewer YourAppletName

You might need to run kbuildsycoca4
in order to get the .desktop file recognized.

If you wish to configure make with a different installation prefix, 
for example the default /usr/local, you may need to adjust the
environment variables
  QT_PLUGIN_PATHS
  KDEDIRS

LICENCE
=======

KDE Internet Usage Meter
Copyright (C) 2013  Terry Moschou <tmoschou@gmail.com>

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

DEVELOPERS
==========

Notes regarding viewing ui in QtCreator:
 Ensure import path in kinum.qmlproject is correct
 Run 
    qmlplugindump org.kde.plasma.core 0.1 /usr/lib64/kde4/imports > \
      /usr/lib64/kde4/imports/org/kde/plasma/core/plugins.qmltypes
      
    and the same fore each other package

Porting to Plasma 2:
 use helper tool
 plasma-framework/src/tools/port-plasma2.sh
 plasma-framework/src/tools/port-*.sh

 https://community.kde.org/Frameworks/Porting_Notes
 https://community.kde.org/Plasma/PortingTolibplasma2
 
DataEngine 
 run plasmaengineexplorer

BACKENDS
========

* Internode

Please note that Internode have requested that I do not include their API
Document. If you wish to create your own usage meter or support this one, do
not copy the interface from this progam, please contact Internode via
http://www.internode.on.net/contact/support for the API document. Internode 
would like you to contact them directly so that they can record your details
and provide you with updates in the future if necessary.

