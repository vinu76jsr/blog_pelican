Title: Change your NTFS / windows drive label via linux
Date: 2008-06-09 16:02
Category: Tech
Tags: tech, linux, troubleshooting
Slug: change-ntfs-label-linux
Author: Vaibhav Mishra
Summary: Change windows NTFS label in Linux

In my current ubuntu machine suddenly music stops playing after a reboot,
and I figured out that it is the issue of my library, 
My music library was on a *NTFS drive* with label `NEW LABEL` (I never renamed it.), 
and there was another drive on my system with the same label , so whenever I rebooted ubuntu 
append one of the drive (randomly) with **_** so they would be mounted on

    /media/NEW VOLUME
    /media/NEW VOLUME_
  
if I am lucky then my music collection directory is mounted without `_`, 
so with help of IRC guys i figured out a way to counter this,
just install the program `ntfsprogs`.
 
    :::bash
    sudo apt-get install ntfsprogs
 
it'll come up with a program called `ntfslabel`, now type ntfslabel on console to check response, 
if it is installed , it's help would appear, otherwise a messsage saying, `command not found` or `program not installed` will appear,

unmount all your ntfs drives,(I hope u know how to do it)

    :::bash
    sudo umount <drive directory>
    
after unmounting your drives type this on console,

    :::bash
    sudo ntfslabel -f /dev/sda5 <newlabel>
    
 
in your case /dev/sda5 is the drive you want to rename,and new label is any valid string, I supplied books.

    :::bash
    sudo ntfslabel -f /devsda5 books
    
use with caution since we are using -f flag so it'll forced to do it, but this gets the work done.