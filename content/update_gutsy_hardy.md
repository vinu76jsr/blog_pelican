Title: Ubuntu Update from Gutsy to hardy
Date: 2008-04-12 16:23
Category: Tech
Tags: tech, ubuntu
Slug: ubuntu-upgrade-gutsy-hardy
Author: Vaibhav Mishra
Summary: Ubuntu upgrade gutsy to hardy.


Today I visited ubuntu site and saw the ubuntu counter, that moment I realized that hardy release is around the corner
and I should now upgrade my gutsy to hardy so that i will not have slow speed ubuntu servers download problem that was there last year
during the release of gutsy, the developer community suggested then it is safe to upgrade to next distribution few days before 
the final release release date to beta version because that beta is almost complete and normal update m
anager will than easily update you to full release, here are my next few steps which may result in a nice how to to 
upgrade from ubuntu gutsy to ubuntu hardy

- I used the shortcut of run in ubuntu i.e., Alt-f2(you can type the following commands in regular shell but do it 
with sudo or in superuser account) then on the popped upcd  window I typed `sudo update-manager --devel-releases` 
( ps:I m not sure it is release or releases but because currently my system is updating I cannot crosscheck).

- this will pop your update manager and if not than you should try above command with `sudo` prefixed.

- now the update manager will load its package list and make sure it show you that your system is up-to-date.
If not than first update your system before following because it is strongly suggested by official ubuntu 
community documentation,I really don't know what will happen if you don't do it.

- when you make sure that update manager show that your system is up-to-date click on the 
check button (it's a button with check written over it, duh!).

- before the next step make few checks.
    
    - your root partition have 2 gb of free space if not than free your space because hardy had to download 1.5 gb in my system, 
    yours may be more or less.
    
    - if you cant free the space than delete the contents of folder `/var/cache/apt/archives` except
     the partial folder (because it is essential for apt to function properly), 
     it might be over 1 gb based on how much you downloaded additional packages form the 
     repositories (remember this step is only to free up space, if you have free space than no need to do this).
     
    - when the check is finished there will be a section which shows distribution update, 
    use it  and upgrade will start, now sit back nad relax because it will take an awful 
    lot of time and will ask you few questions(in my case msttcorefonts package did not 
    get installed but it is ok for me it never did get installed before).
    
    - after say 6 to 12 hours your system will get updated (at this time mine is in its 13th hour 
    and it is not even half so dont believe me).
    
    - restart your system and enjoy your shiny new OS.