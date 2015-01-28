# debian-preseed
This is a preseed file I use to deploy Debian servers. It should live on a webserver that your servers can reach. If you often deploy servers to different many different types of hardware you may prefer this method for provisioning new servers. This approach works very well when coupled with a configuration management service like Puppet or Salt. *By default this installation file will completely wipe the first hard drive* and create an LVM volune. 

## Notes about this file
- This file will install a minimal installation of Debian.
- You can use mkpasswd *(apt-get install whois)* to generate a static password for root and first user
- Feel free to take and customize it.

## How to use this preseed file
1. Place this preseed file on an accessable webserver.
2. Boot your desired version of Debian.
3. At the graphical installation selection screen press the 'Escape' key.
  <img src="https://raw.githubusercontent.com/artsturdevant/debian-preseed/master/debian-boot-screen.png">
4. type: auto hostname=theNameofYourComputer url=http://yourwebserverURL/preseed.cfg
  <img src="https://raw.githubusercontent.com/artsturdevant/debian-preseed/master/debian-preinstall.png"> 
5. hit 'Enter'
6. Get a coffee
7. Enjoy your new server.
