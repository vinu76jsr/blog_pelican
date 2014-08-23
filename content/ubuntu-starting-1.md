Title: Things to do after installing ubuntu - part 1
Date: 2010-11-11 9:36
Category: Tech
Tags: tech, ubuntu
Slug: ubuntu-getting-started-1
Author: Vaibhav Mishra
Summary: Ubuntu getting started 1.


<div dir="ltr" style="text-align: left;" trbidi="on">
After every major version of ubuntu, there is a surge of re-installation for no particular reason, I am one of these guys, and here is some of the things I do after every installing ubuntu from CD<br />
<br />
<pre class="brush:bash">sudo apt-get update;</pre>
<pre class="brush:bash">sudo apt-get install ubuntu-restricted-extras;</pre>
<br />
ubuntu-restricted-extras is a meta-package which install some of the very needed packages if you are not a puritan, which includes but is not limited to mp3 support, microsoft fonts, and several other goodies, seems like latest version is not as wider a package as we had in lucid and predecessors but it is still useful <br />
<br />
The next thing I do is install sun-jdk, which is out of pure habit now, back in the early days the default installed openjdk had some problem handling jnlp however I think it's not the case now, but what the hell just install sun-jdk till we have it's access<br />
<br />
<pre class="brush:bash">sudo apt-get install sun-java6-jdk;</pre>
<br />
now we will point default java to sun jdk<br />
<br />
for this type this on the terminal<br />
<br />
<pre class="brush:bash">sudo update-alternatives --config java</pre>
<br />
and select the option which refer to sun-jdk<br />
<br />
and you have almost everything,<br />
<br />
and now the adobe flash player<br />
<br />
<pre class="brush:bash">sudo apt-get install flashplugin-nonfree</pre>
<br />
and now add some lines in .bashrc file , it is located in your home folder<br />
, replace gedit by nano or vi if you prefer command line<br />
<br />
<pre class="brush:bash">gedit ~/.bash_aliases</pre>
<br />
and add following lines<br />
<br />
<pre class="brush:bash">alias search='apt-cache search ';
alias install='sudo apt-get install ';
alias remove='sudo apt-get remove ';
alias autoremove='sudo apt-get autoremove';
alias clean='sudo apt-get clean ';
alias autoclean='sudo apt-get autoclean';
</pre>
<br />
alias is kind of a shortcut for a long command for example<br />
if you want to install build-essential package<br />
instead of writing<br />
<pre class="brush:bash">sudo apt-get install build-essential;</pre>
one can simply write<br />
<pre class="brush:bash;">install build-essential;</pre>
<br />
<br />
This is the end of part 1 , in next part we do some optional stuff.<br />
<br />
update:<br />
<a href="ubuntu-getting-started-2.html">here is the link for next part</a></div>
