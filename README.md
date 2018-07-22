# referencer
Gnome Referencer is a software to manage your bibiliography. This software has been originaly written by John Spray <jcspray@icculus.org>.
Referencer has some broken dependencies and is no more available in Debian repositories. This project aims to package Referencer as snap so that it will be possible to install and use it most recent linux distributions. 


In order to build the snap :

install snapcraft (with snap or apt-get)

run,inside this directory (at the same location than the .yaml file), the command : snapraft 

Install the created snap with the command : snap install referencer*** --devmode

run referencer with the command : snap run referencer (or launch it from the dash)

CURRENT KNOWN PROBLEMS :

- 1:Cannot oen external pdf when clicking on the reference
- 2:default directory when clicking on the open dialogue button is unreadble
- 3:Lyx plugin seems to crash due to a syntax error
- 4:Referencer use its english interface and does not detect local language settings
- 5:Size of the snap looks too big

Exploration in order to solve these problems :
- 1:Its a current snap/security limitation. It seems that some dev are ongoing to get xdg-open working. In RefWindow.c, if I make a call to system(xdg-open mypdf) instead of launch_default_for_uri(), that seems working. As I change snap core to edge... maybe the call to launch_default_for_uri() also works now ???
- 1:Port referencer to dconf and package as deb again : that should not be a big deal : see in Preference.h : only few pref use gconf
- 3:could it be related to a missing Lyx installation ?
- 2:that is not critical as we can move form this directory
- 4:Need to post on the forum
- 5:Reduce dependencies by removing desktop-gtk2 but including only necessary dependencies.
