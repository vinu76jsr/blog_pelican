Title: OSX mavericks install_name_tool error
Date: 2014-07-28 14:39
Category: Tech
Tags: tech, osx, troubleshooting
Slug: install-name-tool-error
Author: Vaibhav Mishra
Summary: install_name_tool error

Today my django server stopped connecting to mysql in the local install, this was weird but I thought I must have done
something to trigger this weird problem, this had happened to me before and is usually fixed by just re-installing 
`mysql`, so the next course of action

    :::bash
    brew uninstall mysql 
    brew install mysql
    
but each install comes with following error

    :::bash
    Warning: You have an outdated version of /usr/bin/install_name_tool installed.
    This will cause binary package installations to fail.
    This can happen if you install osx-gcc-installer or RailsInstaller.
    To restore it, you must reinstall OS X or restore the binary from
    the OS packages.
    
this looks like the problem with one of the internal OSX tools, I thought of re-installing Command-line tools, and there 
was a late July release, however that didn't pan out as I expected, the error persisted, after some poking around and 
looking into various suggestions on github's homebrew issue pages the problem seemed to be related to __install_name_tool__
so the next course of aciton was to remove the file

I completely scraped off my homebrew installtion and removed all the packages, then asked one of my co-workers to give me
the said file from their computer, and replaced it.

    :::bash
    sudo rm /usr/bin/install_name_tool
    sudo cp ~/Downloads/install_name_tool .  
    
My file was downloaded to **~/Downloads** location and luckily enough it worked, I reinstalled openssl and mysql and
everything seems to be fine now.

off to development.
Lesson learned : next time take brew doctor warning's seriously.


    
