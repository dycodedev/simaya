
== This is forked version with some changes

## Setup

* Development is on Windows (Yes, I am one of those guys)
* Deploy on Ubuntu

## Changes

* Add os checking (some modules don't work on Windows. current strategy is to comment out those codes)
* Provide two kinds of symbolic link. One from Linux family `ln -s` and other is Windows `mklink`. Start script will handle symbolic link creation (into `ob` and `sinergis`)
* Lots of updates in API v.2
* Use forever instead of nohup in deployment

## Setup on Windows

A bit complicated due to some modules are native and will need to be compiled.

* Make sure Nodejs and MongoDB installed (It is recommended to run MongoDB as daemon)
* Install Visul Studio 2012 (or any other version. Express is fine)
* Install module node-gyp and nodemon (both globally)
* cd simaya
* npm install
* cb ownbox -> npm install -> cd ..
* cb sinergis-base -> npm install -> cd ..
* mkdir uploads
* node toos/init-admin.js to add the first user!
* run the app with start-windows.cmd

## Setup on Linux

* Make sure Nodejs and MongoDB installed
* Install gcc and other stuff (See docs/id/CARA-PASANG.txt)
* Install module node-gyp and forever (both globally)
* cd simaya
* npm install
* cb ownbox -> npm install -> cd ..
* cb sinergis-base -> npm install -> cd ..
* mkdir uploads
* node toos/init-admin.js to add the first user!

Before running with start-linux.sh make note that start-linux.sh assume following things:

* The application folder is $HOME/apps/simaya
* For development, you might want to use nodemon instead




