# MyRaspberryPiAdblocker

## GENERAL
 This is one way to make your own adblocker for you network, by using one raspberry pi and pi-hole.
 
 Pi-hole is a network-level advertisement and Internet tracker blocking application for Linux which acts as a DNS sinkhole intended for use on a private network. It is designed for low-power embedded devices with network capability, focusing on the Raspberry Pi as its 'reference' hardware platform.
 
 In my case i choose to work with Raspberry pi zero which cost about 10$.
 
 ## REQUIREMENTS
 
 * Raspberry Pi
 * Micro SD card (at least 8 GB)
 * Micro Usb cable to power Pi
 * Internet connection
 * USB adapter and cable(if you don't SSH)
 * HDMI(if you don't SSH)
 
 
 ## DESCRIPTION 
 
  ## 1.1 INSTALL RASPBERRY'S  OS  
  Once you have all the components you need, the next step is to install Raspberry Pi's OS.
  * Insert a microSD card / reader into your computer
  * Download and install [Raspberry Pi Imager](https://www.raspberrypi.com/software/) 
  * Select "Choose OS" and from the menu select "Raspberry Pi OS"
  * Click "Choose SD card" 
  * Finally clik "Write"

  ## 1.2 UPDATE-UPGRADE AND INSTALL PI-HOLE
  * Connect to the raspberry over SSH using Putty
    
  * [Download-install](https://www.chiark.greenend.org.uk/~sgtatham/putty/) and open Putty
  * Via PuTTY enter the hostname as raspberrypi.local (on some networks, this is just raspberrypi without the .local) and then click Open
 <p align="center">
 <img width="430" height="430" src="https://github.com/TheodoreGisis/MyRaspberryPiAdblocker/blob/main/pihole/Putty.png" >
 </p>
  
  
  
  
  
  
  
   * Update and upgrade the system 
   
         sudo apt update && sudo apt upgrade -y
       
   * Install Pi-hole 
   
         curl -sSL https://install.pi-hole.net | bash
         
   * During the installation, pi-hole will ask you to configure different options.The first step is to configure your upstream DNS provider(i use GOOGLE).
    <p align="center">
    <img width="560" height="430" src="https://github.com/TheodoreGisis/MyRaspberryPiAdblocker/blob/main/pihole/DNS.jpg" >
    </p>
    
    
   * Pi-hole will prompt you with four lists that you can subscribe to that will automatically block ads. Since ad blocking is Pi-hole’s main attraction, it is              suggested that you subscribe to all the default lists. However, if you’d rather not use these lists, you can add or remove them after Pi-hole has been installed
    
    
    <p align="center">
    <img width="560" height="430" src="https://github.com/TheodoreGisis/MyRaspberryPiAdblocker/blob/main/pihole/DNS.jpg" >
    </p>


