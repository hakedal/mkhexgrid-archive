# mkhexgrid

This repository is a mirror/archive of the
`mkhexgrid` program, version 0.1.1, originally found at
<http://www.nomic.net/~uckelman/mkhexgrid/>.

It hasn't received updates in a number of years but is
still useful. It would be a shame if it were to be lost
should the original site come down. For archival 
purposes, this repository will not be modified. However,
it probably won't build in its current state on most 
machines.

To get it building, try the following:

1. Ensure `boost` and `gd` are available on your system.
2. Execute the following commands, taken from
<https://aur.archlinux.org/packages/mk/mkhexgrid/PKGBUILD>
        
        sed -i -e 's/catch (exception /catch (std::exception /' mkhexgrid.cpp
        sed -i -e '/#include <stdexcept>/ i\
            #include <cstring>' grid.cpp
        sed -i -e '/#include <sstream>/ i\
            #include <cstring>' png.cpp

