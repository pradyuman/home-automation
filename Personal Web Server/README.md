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

Steps:

1. Make sure everything is up to date by running:

```
`sudo apt-get update`
`sudo apt-get upgrade`
```