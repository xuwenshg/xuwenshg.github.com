---
layout: post
title: "Hello Workd"
description: ""
category: 
tags: []
---
{% include JB/setup %}
------------------------------------------------------------------------------
      $ sudo fdisk -lu /dev/sd
      sda   sda1  sda2  sda3  sda5  sda6  sda7  sda8  sda9  sdb   sdb4  
      $ sudo fdisk -lu /dev/sda
-----------------------------------------------------------------------------
Disk /dev/sda: 320.1 GB, 320072933376 bytes
255 heads, 63 sectors/track, 38913 cylinders, total 625142448 sectors
Units = sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 4096 bytes
I/O size (minimum/optimal): 4096 bytes / 4096 bytes
Disk identifier: 0xae021554

   Device Boot      Start         End      Blocks   Id  System
/dev/sda1   *        2048      206847      102400    7  HPFS/NTFS/exFAT
/dev/sda2          206848    85936127    42864640    7  HPFS/NTFS/exFAT
/dev/sda3        85936190   625141759   269602785    f  W95 Ext'd (LBA)
Partition 3 does not start on physical sector boundary.
/dev/sda5        85936192   233198204    73631006+   7  HPFS/NTFS/exFAT
/dev/sda6       233198268   380711938    73756835+   7  HPFS/NTFS/exFAT
Partition 6 does not start on physical sector boundary.
/dev/sda7       380712002   527890128    73589063+   7  HPFS/NTFS/exFAT
Partition 7 does not start on physical sector boundary.
/dev/sda8       612999168   625141759     6071296   82  Linux swap / Solaris
/dev/sda9       527890432   612993023    42551296   83  Linux

Partition table entries are not in disk order
---------------------------------------------------------------------------------
      $ sudo mount /dev/sda9 /mnt
      $ sudo grub-install --root-directory=/mnt /dev/sda
      Installation finished. No error reported.
