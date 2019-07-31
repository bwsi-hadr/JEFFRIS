---
title: 'SSH'
date: 2018-11-28T15:14:39+10:00
weight: 102
---

## What is SSH

SSH is short for Secure Shell. Because a Raspberry Pi is a standalone computer without a keyboard, mouse, or monitor, the question arises: how are you supposed to use the Raspberry Pi? SSH allows a computer to remotely access and run commands on another computer. In this case, a personal computer or team laptop will "SSH" into the Raspberry Pi to write code and run commands.

## Setting up SSH in Linux/MacOS

With a Linux or Mac system you can SSH directly from a terminal.

Open a new terminal and run the following command:
```
ssh pi@raspberrypi.local
```
The format is `<username>@<IP address>`. You will be prompted enter a password, the default password for the Raspberry Pi is "raspberry".

## Setting up SSH in Windows

For Windows systems you will need to install PuTTY, which is a open-source terminal emulator. If you do not already have it installed, you can download it [here](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html).

Once PuTTY is installed, you can open it and input the IP address in the space labeled "Host Name (or IP address)."  Leave the default Port as 22 and than click "Open" at the bottom right of the PuTTY window.

You will be prompted to input a username and password for the Raspberry Pi.
Username Default: pi <br />
Password Default: raspberry <br />

Now you have successfully SSH into the Raspberry Pi!!

# Troubleshooting

## Hostname raspberrypi.local not Resolved

This error occurs when the Raspberry Pi is not properly connected to the computer. Check a few things first:

* The Raspberry Pi is on, and its leftmost micro-USB port has a cable running to the computer. 
* Your computer recognizes the Raspberry Pi as a wired connection. If you're using Ubuntu, open your settings and click the Network tab on the right. Then, check that there is a wired connection. If there isn't, you may need to connect the Pi to a different port on your computer and try again.
* If the connection shows up, click on it and open the IPv4 settings. Change it from Automatic to Link Local only.

If the Pi still does not connect, just try again. The Pi is not a very stable computer, and it may work after multiple attempts.