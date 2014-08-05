Title: Droplet read-only file system issue
Date: 2014-07-02 16:02
Category: Tech
Tags: tech, droplet, troubleshooting
Slug: droplet-read-only-filesystem
Author: Vaibhav Mishra
Summary: Droplet read-only filesystem


Today I came across a weird issue where my blog was not showing any `disqus` comment,
this blog runs on pelican which just has one setting to make `disqus` work for it
    
    :::python
    DISQUS_SITENAME = "vaibhavmishra"
    
the setting was present but comments were not showing up, the first thing which will
come to mind is it might be a theme issue so I thought about changing the theme to `mnmlist`(see the name is also minimal)
to something else, after changing the theme, I ran `fab publish` and then I saw the proble, 
my publish works using `rsync` from my local development setup to the droplet, this used to work
like a charm and I expected the same results now, however that was not the case, the command 
failed with an error message

    :::bash
    rsync: mkstemp "/***/***/***/.archives.html.Z2VFuR" failed: Read-only file system (30)

this seems like a problem with the file system so I ssh\`ed to droplet and thought about running `apt-get update`
before looking into the problem, even that failed, so it seemed like something is fundamentally wrong with the setup
and a quick google search reveals it might be a permission issue, I thought I might have set some 
temporary permission in the past which might be the culprit so let me just reboot the system
after `sudo reboot` and a few minute wait I tried to ssh again into the system, this time
it was flatt-out refusal to let me login, the dreaded connection refused, however these guys provide a web based console from 
their website so I went there to make some meaning of the situation and logged into the web based console,
and voila, it auto-detected the problem, the issue was some corrupted file-system, I asked it to try to fix it and 
everything is now well and good, also the comments issue mentioned in the start is also the theme problem, 
changing theme fixed it automatically.

**update: 23rd July**

this happened again today, seems like DigitalOcean has faulty File System since I hadn't even touched 
my VM since last time, the fix is just reboot the machine or use power cycle feature to reboot it and
then go to console access.

