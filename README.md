# referencer
Gnome Referencer is a software to manage your bibiliography. This software has been originaly written by John Spray <jcspray@icculus.org>.
Referencer has some broken dependencies and is no more available in Debian repositories. This project aims to package Referencer as snap so that it will be possible to install and use it most recent linux distributions. 


In order to build the snap :

install snapcraft (with snap or apt-get)

run,inside this directory (at the same location than the .yaml file), the command : snapraft 

Install the created snap with the command : snap install referencer*** --devmode

run referencer with the command : snap run referencer (or launch it from the dash)

CURRENT KNOWN PROBLEMS :

- Cannot oen external pdf when clicking on the reference
- default directory when clicking on the open dialogue button is unreadble
- Lyx plugin seems to crash due to a syntax error
- Referencer use its english interface and does not detect local language settings
- Size of the snap looks too big  
