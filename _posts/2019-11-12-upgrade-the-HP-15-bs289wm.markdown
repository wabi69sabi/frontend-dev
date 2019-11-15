---
layout: post
title:  "Upgrade the HP-15-bs289wm"
date:   2019-11-12 10:30:00 -0700
categories: course update
youtubeId: zm29Np8JIy4
---

# Upgrade your laptops

It is possible to put in 8GB of RAM and some SSD into the HP laptop that was provide by the course.

This company provides a nice product [detail page](https://www.crucial.com/usa/en/compatible-upgrade-for/HP---Compaq/hp-15-bs289wm) here to find compatible RAM.
But there are many other companies that have compatible RAM as [this search](https://www.amazon.com/s?k=8gb+ddr4-2400+sodimm&crid=1NGS6UDKNN1T3&sprefix=8+gb+ddr4-2400%2Caps%2C228&ref=nb_sb_ss_sc_3_14) shows.

Here is a documentation of how you can go about opening the HP and swapping the memory.

## First step: Opening the laptop

As this step is sometimes scary to people who have not done this before, I always find it helpful to watch some videos of others who have opened the same devise.

{% include youtubePlayer.html id=page.youtubeId %}

This is how mine looked:

![Open Laptop](/frontend-dev/assets/images/open_laptop.jpg)

## Next step: Swap RAM

Once the laptop is open it is pretty easy to find the RAM, just carefully pry the plastic prongs apart that clamp down the RAM.

Here is a picture of old (left) and new (right) RAM.

![Open Laptop](/frontend-dev/assets/images/RAMswap.jpg)

## Final steps: Confirm RAM upgrade

Once you have put everything back together, just boot up the laptop and either confirm in the BIOS or your installed OS, that the memory has been recognized.

Here is a pic of upgraded SysINFO on boot:

![SysINFO](/frontend-dev/assets/images/systemINFO.jpg)

I currently have Manjaro installed on mine, which I can recommend for developers. This is how the system info looks like in the Manjaro console:

![ManjaroSysINFO](/frontend-dev/assets/images/manjaroSYSinfo.jpg)

Here are the running stats:

![ManjaroSysStats](/frontend-dev/assets/images/manjaroStats.jpg)
