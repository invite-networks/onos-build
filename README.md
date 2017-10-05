# ONos Build 
This will build an installer ISO for the Open Network Operating System (ONos)

## Summary

This provides the ability to create and customize an Open Network Operating System (ONos).  ONos uses Debian as the starting point, and we need to build from a working Debian install.  Stretch is what ONos is currently based off of.  The build system does not need to match the release of ONos but it is recommended. 

## Setup

1. Install Debian
2. Install all of the packages needed to build and compile

```
apt-get install -y git autoconf dpkg-dev syslinux genisoimage make lsb-release ssh sudo fakechroot devscripts live-build automake libtool libglib2.0-dev libboost-filesystem-dev libapt-pkg-dev flex bison squashfs-tools libperl-dev libnfnetlink-dev isolinux
```

3. Clone this repo and cd into the newly created dirctory 

```
git clone https://github.com/invite-networks/onos-build.git && cd onos-build
```

4. Edit the settings file to make any changes you need to in your enviroment

5. Download a build package into the package directory.

```
cd packages && git clone https://github.com/invite-networks/onos-base.git
```

6. Build the iso

```
cd ../ && ./build projects/onos-base
```
