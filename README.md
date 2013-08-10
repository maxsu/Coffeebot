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

1. Make sure you've got qemu and git. In debian, this is
   ``` sudo apt-get update && apt-get install git qemu qemu-system ```

##### OS X (Untested!)

1. Download and install XCode: https://itunes.apple.com/us/app/xcode/id497799835?ls=1&mt=12
2. Download and install Ports: http://www.macports.org/install.php
3. Install Qemu and Git
   ```sudo port -v selfupdate
      sudo port install git
      sudo port install qemu +target_arm```


##### Windows

Coffee drinkers are too efficient to use windows. Clearly.

#### Onwards!

1. Get the project.
   ``` git init https://github.com/maxsu/Coffeebot && cd Coffeebot```

2. Get the Raspbian image:
   ``` ./rasbpi-get ```
   - The image can be installed onto the physical Pi as well.
   - It lives in the ./raspbian subdirectory.
   
3. Provision the VM:
   ``` sudo ./vm-provision-hard ```

4. Tada! Start your VM:
   ```echo "take the red pill" && ./vm-up ```

#### Inside your VM

1. Run the manual provisioner
   ``` cd ~/project/Coffeebot && vm-provision ```




