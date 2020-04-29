---
layout: post
title:  "Dual boot your HP-15-bs289wm"
date:   2020-04-28 13:31:00 -0700
categories: course update
---

# Dual Boot Your Laptop!

The HP-15-bs289wm comes with a pretty generous 1TB hard drive which allows for comfortable partition. Personally I split mine into three, one Windows partition and two linux partitions. The easiest way to partition and dual boot this laptop is to create a bootable USB drive. Any old USB stick of 8GB or more will do.


Before we create our bootable USB stick, we have to decide on a Linux flavor though. The three most recommend flavors for newbies (in my humble opinion) are:

- [Linux Mint](https://linuxmint.com/)
- [Ubuntu](https://ubuntu.com/)
- [Manjaro Linux](https://manjaro.org/)


A few words about each of these:


Linux Mint --> very sleek and basic linux version that works out of the box. Based on [debian](https://www.debian.org/), which means it is similar to Ubuntu. For Windows users this distro (flavor) might be a bit easier to get started with since the layout is similar to Windows, but keep in mind that the layout is fully customizable and can be changed to the users liking.


Ubuntu --> probably the most 'common', or best known starter flavor for linux. Also based on debian which means it uses the [aptitude](https://packages.debian.org/buster/aptitude) package manager, which makes it fairly easy for new users to install, update and manage software.


Manjaro Linux --> definitely the most 'sophisticated' flavor between the three. This distro is based on [Arch linux](https://www.archlinux.org/), which has a steeper learning curve than debian flavors, but in return is more lightweight (which can translate into better performance and stability) and flexible.

## Create a bootable USB stick in Windows

There are plenty of tools that can create a bootable medium to install linux. Currently [Balena Etcher](https://etcher.download/) is quite popular, but some people might still prefer the more retro GUI from the [Win32 DiscImager](https://win32diskimager.download/). Both of these tools will get the job done. Just download the ISO from the linux website (download section), open Balena Etcher or win32diskimager, select your ISO and USB stick and create a bootable USB stick. Then simply reboot your laptop and press the escape button while booting. From the menu select the USB drive to boot and you should be able to launch a live desktop of your linux flavor.

## Partition the hard drive

Unless you want to completely erase Windows and replace it with linux (not really recommended unless you are a longtime linux user), you should now partition your drive. Some distros (probably all of these) will let you partition while installing by picking the 'install alongside Windows option'. Therefore you could just pick the 'install distro' option from the menu and follow the steps. If you still would like the partition ahead of installing (sort of recommended), you might want to start the live distro with the USB stick and open the console (usually by pressing alt + ctrl + t, or just selecting it in the GUI), just enter ``` sudo gparted ``` and run the graphical partition tool. Then go on with the installation after that.
