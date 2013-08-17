Coffeebot
=========

A coffee server built on Raspberry Pi. 

The idea is to run a small webserver that allows a user to use the internet to tell their coffee machine,

```Make me some Coffee, Please.```

For a top level view of the project tasks check out the project's issues [Kanban](https://waffle.io/maxsu/coffeebot). [![Stories in Ready](https://badge.waffle.io/maxsu/coffeebot.png)](http://waffle.io/maxsu/coffeebot) 

--------------------
====================


### The VM
To test the coffebot server features, we've got a Qemu VM that runs a Raspberry Pi operating system.
VM configuration code should work for the physical device.

#### Install
We've got a couple prereqs to fetch

##### Linux 

1. Make sure you've got qemu and git. In debian/ubuntu, this is:

```
sudo apt-get install git qemu qemu-system
```

##### Os X

1. Get [XCode](https://itunes.apple.com/us/app/xcode/id497799835?ls=1&mt=12) and [Macports](http://www.macports.org/install.php).
2. Get Qemu and Git:

```
sudo port install git qemu +target_arm
```

##### General install
We'll just grab the project and run the setup script
```
git init https://github.com/maxsu/Coffeebot && cd Coffeebot
./vm-get && ./vm-init
```

Note: The provisioning step will require root priviledges. We need
to mount the image and edit some of its configurations.
An alternative that does not need root to edit the contents of the image would be welcome here.

#### Working with the VM

##### Start & Stopping
To start the vm, use ```./vm-up```. On the first run, ignore the `raspi-config` menu.
On subsequent runs, login with the ```pi``` user and password ```raspberry```.

To do a hard shutdown of the machine, you may do ```Ctrl-C``` inside the original terminal window.
This is equivalent to pulling the plug on a physcial Pi.
For a soft shutdown, run ```sudo shutdown -h now``` inside the machine.

If you screw up the machine, you can kill the machine, then run ```./vm-init``` again to get a fresh machine.
This will completely erase the old machine.

##### Admin Work
Aside from that, the machine will behave as a regular, albeit some what slow, Debian machine.
You can for example install packages with ```sudo apt-get update && sudo apt-get install [PACKAGE NAMES]```.

##### Server work

#### [TODO] 
* Give the VM its own IP address or localhost port
* Expand the img to ~3GB
* Preload the img with Coffeebot provisioner code
* Write provisioner code for WP or other (relatively) low overhead page framework



