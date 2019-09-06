# Teonet (CCL) C Containers Library

## 1. Description

The Teonet CCL is a library processed basic containers at C language. The Map and Queue containers are used in [Teonet TR-UDP Library](https://github.com/teonet-co/teonet/wikis/tr-udp).

[![Codacy Badge](https://api.codacy.com/project/badge/Grade/acb5567bad3244f09e96575cf3319516)](https://app.codacy.com/app/angelskieglazki/teoccl?utm_source=github.com&utm_medium=referral&utm_content=teonet-co/teoccl&utm_campaign=Badge_Grade_Dashboard)
[![CircleCI](https://circleci.com/gh/teonet-co/teonet.svg?style=svg&circle-token=d8827ba514cdb37c75565c8e8d7ebd275a0bc167)](https://circleci.com/gh/teonet-co/teoccl)
[![Documentation](https://codedocs.xyz/teonet-co/teoccl.svg)](https://teonet-co.github.io/teoccl/)
[![Download](https://api.bintray.com/packages/teonet-co/u/libteoccl/images/download.svg)](https://bintray.com/teonet-co/u/libteoccl/_latestVersion)


## 2. Installation from sources

### Install dependencies

    sudo apt install libcunit1-dev libcpputest-dev

### Install project with submodules

    git clone git@github.com:teonet-co/teoccl.git
    cd teoccl
    git submodule update --init


### Install Dependences

There is not dependences


### First time, after got sources from subversion repository

    ./autogen.sh


## 3. Make your application 

    make


## 3.1 Using autoscan to Create configure.ac

After make some global changes in sources code use ```autoscan``` to update projects 
configure.ac


## 4. Installation from repository

### UBUNTU

    http://repo.ksproject.org/ubuntu/
    https://dl.bintray.com/teonet-co/u

### Add repository

KSProject:

    sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 8CC88F3BE7D6113C
    sudo apt-get install -y software-properties-common
    sudo add-apt-repository "deb http://repo.ksproject.org/ubuntu/ teonet main"
    sudo apt-get update

Bintray:

    sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 379CE192D401AB61
    echo "deb https://dl.bintray.com/teonet-co/u bionic main" | sudo tee -a /etc/apt/sources.list
    sudo apt-get update

### Install

    sudo apt-get install -y libteoccl

## 5. Run example

See example [README.md](examples/README.md)


## 6. Teo ccl documentation

See libteoccl documentation at: https://teonet-co.github.io/teoccl/
