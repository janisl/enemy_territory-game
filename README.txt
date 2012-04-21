Wolfenstein: Enemy Territory GPL game source
============================================

This file contains the following sections:

GENERAL NOTES
LICENSE

GENERAL NOTES
=============

Game engine:
------------

This release contains only the source of the game DLL files. It was separated
from JLQuake in order to keep it clean and because there are no plans on doing
any improvements on game code. 32 bit game DLLs built from this release should
still be compatible with original engine, but it's recomended to use an improved
game engine such as JLQuake.

Game data and patching:
-----------------------

Wolfenstein: Enemy Territory is a free release, and can be downloaded from
http://www.splashdamage.com/content/wolfenstein-enemy-territory-barracks

This source release does not contain any game data, the game data is still
covered by the original EULA and must be obeyed as usual.

Install the latest version of the game for your platform to get the game data.

Compiling on Windows:
-------------------

A Visual C++ 2010 project is provided in src\wolf.sln.
The solution file is compatible with the Express release of Visual C++.

In order to test your 32 bit binaries, backup and remove etmain\mp_bin.pk3, then
replace etmain\qagame_mp_x86.dll, etmain\cgame_mp_x86.dll, etmain\ui_mp_x86.dll.

On 64 bit Windows copy files qagame_mp_x86_64.dll, cgame_mp_x86_64.dll
and ui_mp_x86_64.dll into etmain directory on Wolfenstein: Enemy Territory install.
You'll need a 64 bit version of JLQuake to run them.

When starting the server make sure to specify 'Pure Server: No' in the advanced
settings page.

Compiling on GNU/Linux and other UNIX based systems:
----------------------------------------------------

mkdir build
cd build
cmake ..
make

In order to test your 32 bit binaries, backup and remove etmain\mp_bin.pk3, then
replace etmain/qagame.mp.i386.so, etmain/cgame.mp.i386.so, etmain/ui.mp.i386.so.

On 64 bit systems copy qagame.mp.x86_64.so, cgame.mp.x86_64.so and
ui.mp.x86_64.so into directory etmain of the Wolfenstein: Enemy Territory install.
You'll need a 64 bit version of JLQuake to run them.

When starting the server make sure to specify 'Pure Server: No' in the advanced
settings page.


LICENSE
=======

See COPYING.txt for the GNU GENERAL PUBLIC LICENSE

ADDITIONAL TERMS:  The Wolfenstein: Enemy Territory GPL Source Code is also subject
to certain additional terms. You should have received a copy of these additional
terms immediately following the terms and conditions of the GNU GPL which accompanied
the Wolf ET Source Code.  If not, please request a copy in writing from id Software
at id Software LLC, c/o ZeniMax Media Inc., Suite 120, Rockville, Maryland 20850 USA.
