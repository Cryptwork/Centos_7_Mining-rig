# Centos 7 Ethereum Mining rig with GUI
Simply Because Centos 7 is built for stability. I hope i made this as simple and easy as possible! I could never find a collection of all this information in one place, so here it is.

# Table of Contents 
1. -  Installing Centos 7 
2. -  Disabling Nouveau Driver
3. -  Installing Nvidia Driver
4. -  SSH connection check (that's the lifeline!)
5. -  Installing & compiling GCC 9.1.0 (take a while)
6. -  Creating the mining service and script
7. -  Setting up TigerVNC, because command lines are a pain
8. -  Upgrading SSL to secure Tigervnc
9. -  Overclock and disabling video output 
10. - Port forwarding
11. - Disabling SSHd, X-server
12. - Hardware tweak (power on, remote power outlet, etc)

## Installing Centos 7

First you'll need a bootable usb with your centos 7 on it. As for an example I use centos 7.6 (no longer available from the repositories at centos.org, you'll have to go on a torrent website to download it) and I've disabled kernel update because I run ANSYS R2020 on my mining rig, which is only run on Centos 7.6 or 7.7. Additionnally, if you don't disable kernel update on Centos 7, you'll likley be faced with reinstalling Nvidia driver and reconfiguring GCC to renable Phoenix Miner to run.  
https://wiki.centos.org/Download
  
I personnaly use a Windows machine as a client to communicate with my miner so Rufus is the go to program. Centos-7 is made to be highly customizable. You may choose from the most basic install to a fully loaded server with options and functionallities up to wazoo. 
https://rufus.ie/   
  
If you have access to an Ubuntu/linux machine to do your create your bootable USB, creating a bootable media is even easier.  
https://ubuntu.com/tutorials/create-a-usb-stick-on-ubuntu#1-overview  

Once you've created your bootable media on a usb a key, you can start the install process. First make sure to log in the bios of your machine to select you bootable USB. Following that portion you'll need to follow with the step to install Centos 7 on your mining machine. Here's a good one:  
https://phoenixnap.com/kb/how-to-install-centos-7    

I like to select Server with GUI, Java support, Compatibilities libraries, Development Tools, System availabilities, High availability, Etc. Of course the more package you'll select the longer boot will take, but once the system is well tuned, booting time won't be of consequence, because you won't have to reboot, period.   

Special notes: make sure you give your user adiministrator access and enable your network connection during the install. There are gazillion of possibilities of configuration for Centos 7. I personnally never tried the minimal install/mining rig combo.  

Once the install has been completed properly, reboot should get Centos 7 started with nouveau driver. If you've decided to lock in the kernel as I did to run something like Ansys. You can run ```no_update_kernel.sh``` as root. It will disable kernel update and run an update for you. 

##  Disabling Nouveau Driver  
Centos 7 come with the nouveau driver, which is no good for mining, but you'll need to disable it in order to install Nvidia Driver. Run ```Disable_Nouveau_Driver.sh``` to get this done. https://wiki.cdot.senecacollege.ca/wiki/CentOS7_Disable_Nouveau for the code! 

3. -  Installing Nvidia Driver
4. -  SSH connection check (that's the lifeline!)
5. -  Installing & compiling GCC 9.1.0 (take a while)
6. -  Creating the mining service and script
7. -  Setting up TigerVNC, because command lines are a pain
8. -  Upgrading SSL to secure Tigervnc
9. -  Overclock and disabling video output 
10. - Port forwarding
11. - Disabling SSHd, X-server
12. - Hardware tweak (power on, remote power outlet, etc)
