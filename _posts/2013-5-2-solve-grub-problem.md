---
layout: post
title: "Solve ubuntu-amd64 grub rescue problem"
description: ""
category: 
tags: [ubuntu]
---
{% include JB/setup %}
------------------------------------------------------------------------------
      $ sudo fdisk -lu /dev/sd
      sda   sda1  sda2  sda3  sda5  sda6  sda7  sda8  sda9  sdb   sdb4  
      $ sudo fdisk -lu /dev/sda
-----------------------------------------------------------------------------


         Device Boot      Start         End      Blocks   Id  System
      /dev/sda8       612999168   625141759     6071296   82  Linux swap / Solaris
      /dev/sda9       527890432   612993023    42551296   83  Linux


---------------------------------------------------------------------------------
      $ sudo mount /dev/sda9 /mnt
      $ sudo grub-install --root-directory=/mnt /dev/sda
      Installation finished. No error reported.
