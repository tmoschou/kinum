Kinum
=====

The KDE Internet Usage Meter

Intially intended as the KDE Internode Usage meter, Kinum will
serve as a pluggable popup applet that can support multiple
backends for different internet service provides (for example 
Internode, iiNet, etc.)


Authors
=======

Terry Moschou <tmoschou@gmail.com>

Build Instructions
==================

cd /where/your/applet/is/installed
mkdir build
cd build
cmake -DCMAKE_INSTALL_PREFIX=$KDEDIRS .. 
make 
make install

(your $KDEDIRS is where you install your KDE 4)

Restart plasma to load the applet 
kquitapp plasma
plasma

or view it with 
plasmoidviewer YourAppletName

You might need to run kbuildsycoca4
in order to get the .desktop file recognized.


Licence
=======

Kinum is Copyright (C) 2012 by Terry Moschou <tmoschou@gmail.com>

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 2 of the License, or
(at your option) any later version.

See the file LICENCE for details.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>
