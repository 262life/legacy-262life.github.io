# Firmware Upgrade

***Editor's Note (7/24/2021):*** _We have updated this tutorial to include how you can boot your_ ***Raspberry Pi 400*** _from USB._

By default, [Raspberry Pi](https://www.tomshardware.com/news/raspberry-pi) boots up and stores all of its programs on a microSD memory card, which has a maximum theoretical bandwidth of 50 MBps on the [Raspberry Pi 4](https://www.tomshardware.com/reviews/raspberry-pi-4) and just 25 MBps on prior models. In real-life, even the [best microSD cards for Raspberry Pi](https://www.tomshardware.com/best-picks/raspberry-pi-microsd-cards) get no faster than about 38 MBps in sequential writes.  Using an external SSD as your main storage drive could speed things up significantly and, with a few commands and a simple firmware update, you can do just that.

In our real-life [tests of a Raspberry Pi 4 with SSD](https://www.tomshardware.com/news/raspberry-pi-4-ssd-test,39811.html) last year we got impressive performance with sequential transfer rates as high as 140 MB / 208 MBps for reading and writing. You can also use a standard USB flash drive, though we found the performance worse than a microSD card on many tasks.

## How to Boot Raspberry Pi 4 / 400 from USB

If you want to start with a fresh install of Raspberry Pi OS, simply follow the instructions in our tutorial on [how to set up Raspberry Pi](https://www.tomshardware.com/reviews/raspberry-pi-set-up-how-to,6029.html) or how to do a Raspberry Pi headless install.

The latest versions of Raspberry Pi OS (as of April 29 2021 or later) have many of the necessary changes built-in. The Raspberry Pi Imager now has a much simpler means to prepare a Raspberry Pi 4 / 400 for USB boot. These instructions will set the Raspberry Pi 4 / 400 to look for a USB boot device, if none is found it will then boot from the micro SD card.

1\. [**Download and install Raspberry Pi Imager**](https://www.raspberrypi.org/downloads/) **from the Raspberry Pi website.**

2\. **Insert a spare micro SD card into your computer.** Note that this card will be erased.

3\. **Launch Raspberry Pi Imager and under Operating System scroll down to Misc Utility Images and left click to open the next menu.**

![b6f9d7442734267ae0033855ba79076e.png](/Users/liottar/Documents/Typora/f4d127213a90496287a54b3c4fb198ab.png)

(Image credit: Tom's Hardware)

4\. **Select Bootloader and then Select USB Boot.** This will return us to the main menu.

![70511ddba6738aadf43a67ff3ca96c83.png](/Users/liottar/Documents/Typora/bcaf49f1621d499aa7f965c999a09dc6.png)

(Image credit: Tom’s Hardware)

5\. **Under Storage click on the button and select the micro SD card.** Double check that you have the right drive before proceeding.

![bcb28992785824b30990340ae123b96a.png](/Users/liottar/Documents/Typora/bcffa68eee3c4c938089e89a0f9fb698.png)

(Image credit: Tom's Hardware)

6\. **Click on Write** to download and write a configuration image to the micro SD card. When done remove the card from your computer.

![1de7a3bb32e7625103e92cb2e1e8c1d9.png](/Users/liottar/Documents/Typora/aa3f7524928e48d49db5d45cb9acd7f5.png)

(Image credit: Tom's Hardware)

7\. **Insert the micro SD card into your Raspberry Pi 4 / 400 and power on.** The green activity light will blink a steady pattern once the update has been completed. If you have an HDMI monitor attached, the screen will go green once the update is complete. Allow 10 seconds or more for the update to complete, do not remove the micro SD card until the update is complete.

8\. **Power off the Raspberry Pi and remove the micro SD card.**

9\. **Into your Raspberry Pi, insert a micro SD card with Raspberry Pi OS and boot from micro SD to the desktop.** This may take a little longer as the Raspberry Pi is looking for USB boot devices. If you do not have a Raspberry Pi OS micro SD card, follow our [how to setup Raspberry Pi](https://www.tomshardware.com/reviews/raspberry-pi-set-up-how-to,6029.html) guide.

10\. **Launch SD Card Copier** from the Accessories section of the start menu. Ensure that your SSD or Flash drive is connected to the Raspberry Pi using a USB 3 port.![5e8735135792eed1d7b90d59df16e6c2.png](/Users/liottar/Documents/Typora/500492e7600e4562a9d8272fb5419f84.png)

(Image credit: Tom's Hardware)

11\. **Select the Copy From Device** (micro SD card), and the **Copy To Device** (the SSD). Double check that the correct drives are selected and **click Start** to copy the files across. The process should take around ten minutes to complete.

![86e11ff3eb5726588535653997bd9268.png](/Users/liottar/Documents/Typora/bc59709d6c6948e4b5829bc84d79cf7d.png)

(Image credit: Tom's Hardware)

12\. **Shut down** the Raspberry Pi.

13\. **Remove the microSD card.**

14\. **Power up** the Raspberry Pi and it will boot from the USB SSD or Flash drive.

![80c00a9c7d43566b50cc2d9d140b957d.png](/Users/liottar/Documents/Typora/fc5bb1b117864e19b863e51d03ddf79b.png)

(Image credit: Tom's Hardware)

Keep in mind that, if you are using an external drive that saps a lot of power from the bus, you may have issues (which you could probably solve by using a drive that has its own power source or by using a powered USB hub).

For example, we had problems using a bus-powered, external Kingston HyperX SSD, which booted but -- perhaps because of how much power it was using -- none of our peripherals would work. A SATA SSD in a externally powered dock worked fine as did a USB Flash drive.

This is an intro