Title: Upgrading Gutsy to Intrepid
Date: 2008-06-09 8:14
Category: Tech
Tags: tech, linux, upgrade
Slug: upgrading-gutsy-intrepid
Author: Vaibhav Mishra
Summary: Test


with the release of intrepid alpha4 I was tempted from several days to upgrade my current hardy to intrepid Ibex, 
but since alpha word is sometimes scary, so be it, I opened my shell
and fired up the upgrade command for the upgrade manager

    :::bash
    sudo update-manager -d

<div dir="ltr" style="text-align: left;" trbidi="on">
<div xmlns="http://www.w3.org/1999/xhtml">

here -d is for development release, the update manager will show if any new distribution even the development release is available, note that they are very much less stable as compared to stable release<br />
<br />
<img src="http://lh3.ggpht.com/vinu76jsr/SMJ1HL9MrcI/AAAAAAAAAw8/14AR9aQkuZU/%5BUNSET%5D.png" style="max-width: 800px;" /><br />
<br />
now your update manager will start and queries the ubuntu repositories for any development release and any other normal task<br />
<br />
<img src="http://lh6.ggpht.com/vinu76jsr/SMJ1mUIGQGI/AAAAAAAAAxA/yHUhIF7F1eA/%5BUNSET%5D.png" style="max-width: 800px;" /><br />
<br />
it shows my system is up to date and there is a new distribution release available, if we had not used the -d option this message will not appear, click on the upgrade button and a new window will pop-up showing you the release note , read it if you want or else move forward<br />
and click upgrade.<br />
<br />
<img src="http://lh5.ggpht.com/vinu76jsr/SMJ2oFEyKzI/AAAAAAAAAxE/L7JdizgTXLU/%5BUNSET%5D.png" style="max-width: 800px;" /><br />
<br />
now a window will show up showing 3rd party resources to be disabled, if you have third party resources enabled , I have plenty of themin repository,if you do not have third party resources enabled no pop-up will show up so next screen-shot may not be there in your upgrade.<br />
<br />
<img src="http://lh6.ggpht.com/vinu76jsr/SMJ3tsqFfbI/AAAAAAAAAxI/wWbs2yfThoI/%5BUNSET%5D.png" style="max-width: 800px;" /><br />
<br />
<br />
you can click close, there is nothing to worry, you can always enable the either by manually editing sources.list or through Synaptic GUI<br />
<br />
<br />
the next screen will show you what is to be removed , how many new packages are to be fetched , it's nice to knwo these stats just for fun<br />
<br />
<img src="http://lh5.ggpht.com/vinu76jsr/SMJ4ktOA8QI/AAAAAAAAAxM/QYBRb--0hU8/%5BUNSET%5D.png" style="max-width: 800px;" /><br />
<br />
i f you click on the details , package list can be seen, this list is somewhat comprehensive and boring , but to know what's new in the new release , it's nice place to have a look, if you had skipped release notes<br />
<br />
<img src="http://lh6.ggpht.com/vinu76jsr/SMJ5Ak-NVwI/AAAAAAAAAxQ/wqLXjb3obSw/%5BUNSET%5D.png" style="max-width: 800px;" /> <br />
<br />
<br />
click on start upgrade, and your upgrade process will start .<br />
<br />
<img src="http://lh6.ggpht.com/vinu76jsr/SMJ5kVaaG0I/AAAAAAAAAxU/-tVnOdlezQY/%5BUNSET%5D.png" style="max-width: 800px;" /><br />
<br />
<br />
next several screens were part of upgrade process chronologically<br />
<br />
The upgrade took place in 6 stages<br />
<ol>
<li><strong>Preparing to upgrade :  here server is queried for changes.</strong></li>
<li><strong>Setting new software channels</strong> : The repositories are arranged to point to right direction.</li>
<li><strong>getting new packages</strong> : packages are downloaded.</li>
<li>i<strong>installing the upgrades</strong> : the downloaded packages are installed.</li>
<li><strong>Cleaning up</strong> : cache is cleaned and obsolete content is removed to save space</li>
<li><strong>Restarting up</strong> : just like windows stuff, but hey! we are upgrading to a new distro so this is not a big deal.</li>
</ol>
<img src="http://lh6.ggpht.com/vinu76jsr/SMKAw2U0jjI/AAAAAAAAAxY/aFS0EY44T74/%5BUNSET%5D.png" style="max-width: 800px;" /><br />
<br />
<img src="http://lh4.ggpht.com/vinu76jsr/SMKBDrXz8tI/AAAAAAAAAxg/QfX5oRdVvOw/%5BUNSET%5D.png" style="max-width: 800px;" /><img src="http://lh6.ggpht.com/vinu76jsr/SMKBsx0QB7I/AAAAAAAAAxk/CS-H8Cv5vm8/%5BUNSET%5D.png" height="695" style="max-width: 800px;" width="605" /><br />
<img src="http://lh5.ggpht.com/vinu76jsr/SMKB0cwNCwI/AAAAAAAAAxo/dHWztd0UKRA/%5BUNSET%5D.png" style="max-width: 800px;" /><img src="http://lh4.ggpht.com/vinu76jsr/SMKA29oKbtI/AAAAAAAAAxc/lq7FFyj6uy0/%5BUNSET%5D.png" style="max-width: 800px;" /><br />
<br />
<img src="http://lh3.ggpht.com/vinu76jsr/SMKCXud6GiI/AAAAAAAAAxs/KsmCIpkcEY8/%5BUNSET%5D.png" style="max-width: 800px;" /><br />
<br />
in the last two screen terminal option is accesible and it show the differences between the two , the second screen just do the stuff, but the one with terminal showing will show you what's going on behind the hood.<br />
<br />
This all stuff will take a while, in mycase it takes slightly more than 3 hours, , from night 1 to 4, in the meantime I had some snacks completed few chapters of Netbeans API and watched a movie, that's the joy of linux, in all of this my network manager crashed, but that is understood because system files are going in and out in the meantime , so this message might pop-up several times  just click Ok each time or let it be there , it will not interfere in your upgrade process since it will appear during 4th step and at that point update - manager had downloaded all required stuff from the internet.<br />
<br />
<img src="http://lh6.ggpht.com/vinu76jsr/SMKEsoStffI/AAAAAAAAAxw/Avod2ITqNh4/%5BUNSET%5D.png" style="max-width: 800px;" /><br />
<br />
<br />
some more screens <br />
<br />
<img src="http://lh6.ggpht.com/vinu76jsr/SMKF7RpO9yI/AAAAAAAAAx0/M1n0IqbDYn8/%5BUNSET%5D.png" height="725" style="max-width: 800px;" width="631" /><br />
<br />
<br />
<img src="http://lh6.ggpht.com/vinu76jsr/SMKGC4ucBcI/AAAAAAAAAx4/xf7mUj_6SfY/%5BUNSET%5D.png" height="728" style="max-width: 800px;" width="633" /><br />
<br />
<br />
<img src="http://lh6.ggpht.com/vinu76jsr/SMKGf6rgdNI/AAAAAAAAAx8/yf8fN2pIcr0/%5BUNSET%5D.png" height="711" style="max-width: 800px;" width="619" /><br />
<br />
in the cleaning up process following window will appear , it serves as a message that obsolete message are to be deleted.<br />
<br />
<img src="http://lh4.ggpht.com/vinu76jsr/SMKHH35etbI/AAAAAAAAAyA/PHS0mz81zu0/%5BUNSET%5D.png" style="max-width: 800px;" /><br />
<br />
<br />
click details to see list of packages to be removed.<br />
<br />
<img src="http://lh5.ggpht.com/vinu76jsr/SMKH5M7-ABI/AAAAAAAAAyE/_kRvZbbHh34/%5BUNSET%5D.png" style="max-width: 800px;" /><br />
<br />
click remove to carry out processes, <br />
<br />
<img src="http://lh4.ggpht.com/vinu76jsr/SMKIUmnTbHI/AAAAAAAAAyI/OE9ZfBcfxlU/%5BUNSET%5D.png" height="628" style="max-width: 800px;" width="546" /><br />
<br />
<br />
It removes the old kernels and other stuff, sit back and enjoy the show<br />
<br />
for the informed , it'll ask you several times to replace some files especially configuration files, and it is up to you how important are your current configuration settings, it asked me for smb.conf and I replaced the original version because I had not much edited the file except sharing some of the directories, and I prefer editing the file over breaking the system altogether with old versions considering the fact that I am risking lot by using alpha release.<br />
<br />
just do what you want to and remember that network pop-up will keep occurring , so ignore it, during installation your network will stop working but it is OK , all your computer will work for sure.<br />
<br />
after a while it will ask for a reboot(at least it did in my case).<br />
<br />
<img src="http://lh5.ggpht.com/vinu76jsr/SMKdy2kvbvI/AAAAAAAAAyM/Tm58fC6Dsq4/%5BUNSET%5D.png" style="max-width: 800px;" /><br />
<br />
<br />
save your work and click restart Now button, and that's it you will now be greeted with new Intrepid installation with grub listing development release kernel, boot from the first in the list, this is pretty much for today I'll post about my experience after reboot in my next post..!!<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br /></div>
</div>
