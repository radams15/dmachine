# DMachine - Docker machines with X forwarding for OSX.


## Prerequisites

First, install docker - I used [colima](https://github.com/abiosoft/colima/)

Next, install XQuartz - I used the one from [MacPorts](https://ports.macports.org/port/xorg-server/): `sudo port install xorg-server`

Next, enable nonlocal access for XQuartz. For the MacPorts version: `defaults write org.macports.X11.plist nolisten_tcp -bool false`

## Usage

#### Creating a machine (A fedora 36 box named dev)

`dm-create dev fedora:36`

#### Entering the new machine

`dm-enter dev`

#### Running nautilus from the machine

`dm-enter dev nautilus`

#### Creating a launcher app for nautilus named 'Dev Nautilus'

`dm-mkapp dev 'nautilus' 'Dev Nautilus'`

#### Deleting a machine

This has not been implemented as a dm tool yet so just delete the machine as you would in docker:

`podman stop dev`

`podman rm dev`
