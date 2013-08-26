---
layout: page
title: "Koding: Rsync"
comments: true
sharing: true
footer: true
---


Keep directories syncronized on Koding with rsync
==================================================
A very common question on the Koding stream is how to upload files to your Koding vm.  This will show you how to do that, but it will also show you how to keep a local directory in sync with a directory on Koding.  This will allow you to back stuff up, work locally, or just get stuff uploaded to Koding.  There are a few different ways to do this, but the tool we're going ot use is [rsync](http://rsync.samba.org/).

**First:** install rsync on your local computer, look [here](http://rsync.samba.org/download.html) for pre-compiled binaries.  If you you're running OSX I recommend installing it using homebrew or macports.

**Second:** Make sure that you can ssh into your koding vm, excellent tutorial on how to do this [here](http://koding.github.io/docs/guides/ssh-into-your-vm/).  *Note: I'm an OSX/Linux user.  I don't run windows so I'm not sure if the putty instructions set you up correctly*

**Third:** Sync!  There are two commands you'll run.  The first is to sync files from Koding to your local computer.  The second is to sync files from your local computer to Koding.  

First Koding -> you
    rsync -avz --progress --stats -e ssh 'vm-1.skarfacegc.koding.kd.io:/home/skarfacegc/*' .
Second you -> Koding
    rsync -avz --progress --stats -e ssh . vm-1.skarfacegc.koding.kd.io:/home/skarfacegc

Add the **--delete** flag to both commands if you want to delete files on the receiver that don't exist on the sender.  **Be careful with this**