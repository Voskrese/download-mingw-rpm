The download-mingw-rpm.py script makes it easy to download compiled binaries
from the windows:mingw[1] project on the OpenSUSE Build Service.

The script needs Python 3 and the 7z program in the path.  The 7z program is
available for POSIX platforms[2] and for Windows[3].  On Debian/Ubuntu derived
distros it's a `sudo apt-get install p7zip-full` away.


EXAMPLES
--------

Download and unpack and rpm from the windows:mingw:win32 project:

./download-mingw-rpm.py zlib

You'll now find a zlib1.dll file in a subdir of the current directory.


A more complicated example to make a zipfile containing pulseaudio with its
dependencies:

old

`./download-mingw-rpm.py -p home:mkbosmans:mingw32:pulseaudio --deps -z pulseaudio`

**new**

`./download-mingw-rpm.py -p home:mikedep333:branches:home:mkbosmans:mingw32:pulseaudio --deps -z pulseaudio`

-------------------------------------------------------------------------------

1) https://build.opensuse.org/project/show?project=windows%3Amingw%3Awin32
2) http://p7zip.sourceforge.net/
3) http://www.7-zip.org/

https://raw.githubusercontent.com/robol/MPSolve/master/tools/download-mingw-rpm.py
