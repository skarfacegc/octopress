---
layout: page
title: "OSX software"
date: 2013-04-05 11:41
comments: false
sharing: true
footer: true
---

I'm frequently asked what software a new OSX user should grab.  I've been mailing this list around 
but I figured it was time to put it in one place I could send people.  Here's the current list:

- **[App Cleaner](http://www.freemacsoft.net/appcleaner/)** This is one of those apps that really should have shipped with the OS.  Watches for applications getting put into your trashcan, asks if you want to delete the rest of the related files (configs, etc).  This is the first thing I install on fresh boxes.
- **[iTerm2](http://www.iterm2.com/)** This is hands down the best terminal program I've used.  Yeah, there's some odd features (instant replay), but there's also great stuff like tmux integration.  Save your config to dropbox to sync between multiple machines.
- **[Cyberduck](http://cyberduck.ch/)** Decent ftp, sftp, webdav, aws, etc file transfer utility.  It's not something I use a ton, but always gets the job done.
- **A Launcher** I'm using [Launchbar](http://www.obdev.at/products/launchbar/index.html) , but there are many.  [Alfred](http://www.alfredapp.com/) seems to be a very popular choice.  I haven't played with it.  [QuickSilver](http://qsapp.com/) is the granddaddy of these.  I used it for quite some time, but stopped due to stability issues and lack of updates.  The project has been taken over and is active again.  Worth a look. 
- **[Adium](http://adium.im/)** Your multi-protocol instant messaging client.  Like trillian.  I'm using the built in messages app due to iMessage integration.  If you don't use an iPhone I'd recommend adium over the built in.
- **[1password](https://agilebits.com/onepassword) $$** This is a fantastic password manager.  It will generate, track, and auto fill (website) passwords.  Can sync via dropbox.  Usable on IOS, windows, OSX, and Android.  Lets you use random & different passwords on each site you use.  About as un-obtrusive as you can get with software like this (imo).
- **Unix Utility Installer** Makes installing your favorite command line (and X11) utilities easy.  Similar to installing software on your favorite unix platform.  There are two choices here.  [MacPorts](http://www.macports.org/) and [HomeBrew](http://mxcl.github.com/homebrew/), I'm using macports. [Read a bit](https://www.google.com/search?q=macports+vs+homebrew), pick for yourself.  Why I like macports:
    - Builds it's own libs  (updating your OS has less risk of breaking your installed programs)
    - Installs in it's own sandbox /opt rather than /usr/local
    - I'm already using it, and it hasn't pissed me off enough to switch.
- **[XQuartz](http://xquartz.macosforge.org/landing/)** X11 Server.
- **[iStat Menus](http://bjango.com/mac/istatmenus/) $$** Put CPU, MEM, Network, etc activity graphs in your menu. 


- 2013/04/05 - initial version.
