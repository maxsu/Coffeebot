Coffeebot
=========

A coffee server built on Raspberry Pi. 

The idea is to run a small webserver that allows a user to use the internet to tell their coffee machine,

```Make me some Coffee, Please.```

#### Contributing to the Project
For now the project consists of Lindsey, Billy, and myself.

For a top level view of the project tasks check out the project [Kanban](https://waffle.io/maxsu/coffeebot). [![Stories in Ready](https://badge.waffle.io/maxsu/coffeebot.png)](http://waffle.io/maxsu/coffeebot) 


### Installing The VM

#### OS Specific Prerequisites

##### Linux

1. Make sure you've got qemu and git. In debian/ubuntu, this is:

```sudo apt-get update && apt-get install git qemu qemu-system```

##### OS X (Untested!)

1. Download and install [XCode](https://itunes.apple.com/us/app/xcode/id497799835?ls=1&mt=12) and [Macports](http://www.macports.org/install.php).
2. Install Qemu and Git

```sudo port -v selfupdate
      sudo port install git qemu +target_arm```


#### Onwards!

```
#Get the project.
git init https://github.com/maxsu/Coffeebot && cd Coffeebot

# Get the Raspbian image ans provision the VM:
./rasbpian-get

# Tada! Start your VM:
echo "take the red pill" && ./vm-up
```

#### Inside your VM

1. Run the manual provisioner

``` cd ~/project/Coffeebot && vm-provision ```




