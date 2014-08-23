Title: Ubuntu android development getting started
Date: 2010-11-11 20:53
Category: development
Tags: development, ubuntu
Slug: ubuntu-android-development
Author: Vaibhav Mishra
Summary: Ubuntu android development getting started.


<div dir="ltr" style="text-align: left;" trbidi="on">
This post is only for android developers <br />
<br />
The first thing to do after installing ubuntu and setting up multimedia options  is setting environment for android development, here are the steps to take -<br />
<br />
<b>Step 1 : install sun java and set it as default</b><br />
<br />
Android doesn't play nice with openjdk which comes as default install in ubuntu , to install it run the following command in the terminal<br />
<br />
<span class="Apple-style-span" style="font-family: 'Courier New',Courier,monospace;">sudo apt-get install sun-java6-jdk</span><br />
<br />
<span class="Apple-style-span" style="font-family: inherit;">This will take some time to install sun java6 jdk and prompt you to agree to DLJ license, just accept it.</span><br />
<b>Step 2 - set sun-java as default</b><br />
<br />
Now set this jdk to be as default , enter this command in bash prompt (Application&gt;Accessories&gt;Terminal) <br />
<br />
<span class="Apple-style-span" style="font-family: 'Courier New',Courier,monospace;">$ sudo update-alternatives --config java</span><br />
<br />
something like this will appear<br />
<br />
<br />
<span class="Apple-style-span" style="font-family: 'Courier New',Courier,monospace;">There are 2 choices for the alternative java (providing /usr/bin/java).</span><br />
<span class="Apple-style-span" style="font-family: 'Courier New',Courier,monospace;"><br />
</span><br />
<span class="Apple-style-span" style="font-family: 'Courier New',Courier,monospace;">&nbsp;&nbsp;Selection &nbsp; &nbsp;Path &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;Priority &nbsp; Status</span><br />
<span class="Apple-style-span" style="font-family: 'Courier New',Courier,monospace;">------------------------------------------------------------</span><br />
<span class="Apple-style-span" style="font-family: 'Courier New',Courier,monospace;">&nbsp;&nbsp;0 &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;/usr/lib/jvm/java-6-openjdk/jre/bin/java &nbsp; 1061 &nbsp; &nbsp; &nbsp;auto mode</span><br />
<span class="Apple-style-span" style="font-family: 'Courier New',Courier,monospace;">&nbsp;&nbsp;1 &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;/usr/lib/jvm/java-6-openjdk/jre/bin/java &nbsp; 1061 &nbsp; &nbsp; &nbsp;manual mode</span><br />
<span class="Apple-style-span" style="font-family: 'Courier New',Courier,monospace;">* 2 &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;/usr/lib/jvm/java-6-sun/jre/bin/java &nbsp; &nbsp; &nbsp; 63 &nbsp; &nbsp; &nbsp; &nbsp;manual mode</span><br />
<span class="Apple-style-span" style="font-family: 'Courier New',Courier,monospace;"><br />
</span><br />
<span class="Apple-style-span" style="font-family: 'Courier New',Courier,monospace;">Press enter to keep the current choice[*], or type selection number:&nbsp;</span><br />
<div>
<br /></div>
<div>
enter number which corresponds to sun jdk , which in my case is 2(although it is laready set here)</div>
<div>
<br /></div>
<div>
<b>Step 3 - Set up android SDK</b></div>
<div>
<br /></div>
<div>
now go to android developer page <a href="http://developer.android.com/sdk/index.html">download the sdk</a>&nbsp;, choose linux version for linux</div>
<div>
<br /></div>
<div>
extract it in ~/dev/devInstall/ (or whichever directory you prefer)</div>
<div>
, now this sdk at it's present for is unusable because it doesnot have any particular version of android platfor installed, enter this into your .bashrc</div>
<div>
<br /></div>
<div>
<span class="Apple-style-span" style="color: #007000;"><span class="Apple-style-span" style="line-height: 13px;"><span class="Apple-style-span" style="font-family: 'Courier New',Courier,monospace;">echo PATH=$PATH:&lt;sdk directory&gt;/tools/</span></span></span></div>
<div>
<span class="Apple-style-span" style="color: #007000; font-family: monospace; font-size: small;"><span class="Apple-style-span" style="font-size: 13px; line-height: 13px;"><br />
</span></span></div>
<div>
<span class="Apple-style-span" style="line-height: 13px;"><span class="Apple-style-span" style="font-family: 'Trebuchet MS',sans-serif;">replace &lt;sdk directory&gt; with ~/dev/devInstall/android-sdk-linux-x86 if you extract android directory to ~/dev/devInstall/</span></span></div>
<div>
<br /></div>
<div>
now run following command&nbsp;</div>
<div>
<br /></div>
<div>
<span class="Apple-style-span" style="font-family: 'Courier New',Courier,monospace;">android</span></div>
<div>
<br /></div>
<div>
this will bring up a GUI from which choose available packages and anyone platform you want to install</div>
<div>
vhoose virtual devices&gt;New and set value as shown in figure</div>
<div>
<br /></div>
<div class="separator" style="clear: both; text-align: center;">
<a href="http://1.bp.blogspot.com/_8IgrExDrA8Y/TNzDfExJ0BI/AAAAAAAAB9M/Y92EoMSAFuk/s1600/Screenshot-Create+new+Android+Virtual+Device+%2528AVD%2529+.png" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"><img border="0" src="http://1.bp.blogspot.com/_8IgrExDrA8Y/TNzDfExJ0BI/AAAAAAAAB9M/Y92EoMSAFuk/s320/Screenshot-Create+new+Android+Virtual+Device+%2528AVD%2529+.png" height="320" width="234" /></a></div>
<div>
<br /></div>
<br />
<span class="Apple-style-span" style="font-family: inherit;"><br />
</span><br />
<span class="Apple-style-span" style="font-family: inherit;">this is a samsung galaxy s like configuration.</span><br />
<span class="Apple-style-span" style="font-family: inherit;"><br />
</span><br />
<span class="Apple-style-span" style="font-family: inherit;">now select available packages and check at least one platform to install.</span><br />
<span class="Apple-style-span" style="font-family: inherit;"><br />
</span><br />
<span class="Apple-style-span" style="font-family: inherit;"><b>Step 4 - Download and set eclipse</b></span><br />
<br />
now go to eclise.org and download ecclipse 3.5.* &nbsp;codenamed galileo , here is <a href="http://www.eclipse.org/downloads/packages/release/galileo/r">link to download page</a><br />
<br />
choose eclipse IDE for java developers because it is the least size from the list which will work fine with android sdk<br />
extract eclipse to ~/dev/devInstall/ and click on ~/dev/devInstall/eclipse to start it, make sure the splash screen show galileo, the current eclipse version is 3.6 which is not yet supported by google,<br />
<br />
choose the default workspace<br />
<br />
when Eclipse is started choose Help&gt;Install New Software...<br />
a window will popup<br />
<br />
<div class="separator" style="clear: both; text-align: center;">
<a href="http://1.bp.blogspot.com/_8IgrExDrA8Y/TNzFQK-mAKI/AAAAAAAAB9Q/ZUwsSwx2UtQ/s1600/Screenshot-Install+.png" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"><img border="0" src="http://1.bp.blogspot.com/_8IgrExDrA8Y/TNzFQK-mAKI/AAAAAAAAB9Q/ZUwsSwx2UtQ/s640/Screenshot-Install+.png" height="480" width="640" /></a></div>
<br />
<span class="Apple-style-span" style="font-family: inherit;">in Work with text enter box, enter the following</span><br />
<span class="Apple-style-span" style="font-family: inherit;"><br />
</span><br />
<span class="Apple-style-span" style="font-family: inherit;"><span class="Apple-style-span" style="border-collapse: collapse; font-family: arial,sans-serif; font-size: 13px; line-height: 16px;"></span></span><br />
<pre class="prettyprint" style="background-color: #fafafa; border: 1px solid rgb(204, 204, 204); color: #007000; font-family: monospace; line-height: inherit; margin: 0.5em 0px 0px 1em; overflow: auto; padding: 10px;"><span class="Apple-style-span" style="font-family: inherit;"><span class="pln" style="color: black;">https</span><span class="pun" style="color: #666600;">:</span><span class="com" style="color: #880000;">//dl-ssl.google.com/android/ecli</span><span class="Apple-style-span" style="color: #880000;">pse/</span></span></pre>
<div style="color: #333333;">
<span class="Apple-style-span" style="font-family: inherit;"><span class="com" style="color: #880000;"><br />
</span></span></div>
<div>
<span class="Apple-style-span" style="font-family: inherit;">click add and wait for some time, A check box titled Developer tools will become available , jsut check it and click on Next, accept the license, installation will start, wait for it to finish , elipse will ask you to restart , select yes and you are almost done, just one minute thing is to be done, pointing eclipse to the location of android sdk directory,</span></div>
<div>
<span class="Apple-style-span" style="font-family: inherit;"><br />
</span></div>
<div>
<span class="Apple-style-span" style="font-family: inherit;">choose Window&gt;Preferences&gt;Android and click on browse button in front of SDK location , select your SDK location ( mine is&nbsp;/home/vaibhav/dev/devInstall/android-sdk-linux_x86</span>&nbsp;) select apply then OK</div>
<div>
<br /></div>
<div>
and you're done,</div>
<div>
<br /></div>
<div>
In next entry I will create a simple hello world in android or you can buy the book.</div>
<br />
<iframe frameborder="0" marginheight="0" marginwidth="0" scrolling="no" src="http://www.flipkart.com/affiliateiframe.php?bc=FFFFFF&amp;tc=000000&amp;lc=A52A2A&amp;buy=&amp;affid=INVaibhNic&amp;id=OU23F8O55D&amp;type=3&amp;price=yes&amp;border=yes&amp;height=260&amp;width=120" style="height: 260px; width: 120px;"></iframe>    <iframe align="left" frameborder="0" marginheight="0" marginwidth="0" scrolling="no" src="http://rcm.amazon.com/e/cm?t=widgetsamazon-20&amp;o=1&amp;p=8&amp;l=bpl&amp;asins=0470565527&amp;fc1=000000&amp;IS2=1&amp;lt1=_blank&amp;m=amazon&amp;lc1=0000FF&amp;bc1=000000&amp;bg1=FFFFFF&amp;f=ifr" style="align: left; height: 245px; padding-right: 10px; padding-top: 5px; width: 131px;"></iframe></div>
