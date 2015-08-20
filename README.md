# ONOS Build 
This will build an installer ISO for the Open Network Operating System (ONOS)

## Summary

This provides the ability to create and customize an Open Network Operating System (ONOS).  ONOS uses Debian as the starting point, and we need to build from a working Debian install.  Jessie RC1 is what ONOS is currently based of off, and will be updated as soon as Jessie is released.  The build system does not need to match the release of ONOS but it is recommended. 

## Setup

1. Install Debian
2. Install all of the packages needed to build and compile

```
apt-get install -y git autoconf dpkg-dev syslinux genisoimage make lsb-release ssh sudo fakechroot devscripts live-build automake kernel-package libtool libglib2.0-dev libboost-filesystem-dev libapt-pkg-dev flex bison libperl-dev libnfnetlink-dev
```

3. Clone this repo and cd into the newly created dirctory 

```
git clone https://github.com/invite-networks/onos-build.git && cd onos-build
```

4. Edit the settings file to make any changes you need to in your enviroment

5. Build the iso

```
./build projects/onos-base
```

## Usage

Reference https://github.com/invite-networks/onos.git for details on how to build an ISO
