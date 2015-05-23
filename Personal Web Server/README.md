# Raspberry Pi Personal Web Server
I created a personal web server to display the control panel of my home automation server.

What is needed:

* Raspberry Pi (I used the RPi 2 Model B+)
* An internet connection
* A way to connect the RPi to the internet (via ethernet or wifi dongle)
* A way to power your RPi
* Access to your router settings

Things that are cool but aren't needed:

* Secure Shell (SSH) access to your RPi
* A registered domain name
* Dynamic DNS service (explained later)

**If you haven't set up your RPi yet, you'll need to grab an SD or microSD card and a keyboard, mouse, and monitor and install an operating system on your Raspberry Pi. I use and recommend Raspbian, but it is possible to set up a web server on any Raspberry Pi operating system. You can follow the directions [here] (https://www.raspberrypi.org/help/noobs-setup/) to install Raspbian.

If you need a more general setup guide or some more help setting up your RPi, go [here] (https://www.raspberrypi.org/help/quick-start-guide/). 

#Setup Instructions:

* Make sure everything is up to date by running:

  ```
  sudo apt-get update
  sudo apt-get upgrade
  ```
  
**Installing Web Server software:**

* I set up my web server using Apache Web server software during my intial setup. It is quick and fast and is a good way to  test if everything is running properly. You can install node.js, nginx, or other web server software once you have tested that all your networking and basic setup is working (node.js in particular takes a few hours to compile and install and is not an efficient way to start). Run the following command to install apache, php, and a library that help Apache work with PHP:

  ```
  sudo apt-get install apache2 php5 libapache2-mod-php5
  ```

* Once Apache is finished installing, go to your web browser (on the RPi or a computer attached to the same network) and type in your RPi's local IP address. To find this ip address, run `ifconfig` and look for *inet address*. This number is your RPi's local IP address. If there were no issues with your setup, a basic web site should load (headlined with "It works!"). If this does not show up, restart the apache service using the following command:

  ```
  sudo service apache2 restart
  ```

  If it still does not work, try uninstalling and reinstalling apache using the following commands:

  ```
  sudo apt-get --purge remove apache2 php5 libapache2-mod-php5
  sudo apt-get autoremove --purge
  sudo apt-get install apache2 php5 libapache2-mod-php5
  ```
