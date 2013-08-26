---
layout: page
title: "Koding: About"
comments: true
sharing: true
footer: true
---

This is about some details that I've been able to figure out about Koding.  This isn't an overview.  Lee Olayvar has put together a really solid overview that can be found [here](http://koding.github.io/docs/guides/koding-overview/).  

- Koding provides access to a linux container running ubuntu.  A container is similar enough to a virtual machine that you can basically think of it as a virtual machine.  However, there are a few key differences that are important to understand. (for more on containers [look here](http://www.linuxjournal.com/content/containers%E2%80%94not-virtual-machines%E2%80%94are-future-cloud))
    - There is only one kernel running.  Most VMs run one kernel per virtual machine.  With a container there is only one kernel.  The virtual machines are segmented at the process level.  All instances share memory and CPU.
    - You can't modify (either through recompilation or through dynlib) the kernel.  This means that adding fuse support to the kernel is something that the Koding folks have to do.
    - I'm not entirely sure what the reboot command does.  It seems to do mostly what you'd think, but your uptime doesn't change.  It also seems to be instant.

- Remote access to your VM goes through a proxy (I'm guessing based on some comments and how the ssh connection works)
    - This is _mostly_ transparent to you.  Except for ...
    - SSL and other encrypted comms have some issues here (this is pretty educated speculation, I haven't tried).  Encrypted channels are generally built to not allow someone to sit in the middle of your connection.  The proxy sits in the middle.  This is why you need to play games with [ssh](http://koding.github.io/docs/guides/ssh-into-your-vm/)
    - SSH require some extra stuff to make it work.  This is fairly unusual, but easy to do (_at least on OSX/linux_). Simply add the following to ~/.ssh/config  (nc is the netcat command, do some googling on it and you should be able to figure out what the below config is doing. It's pretty neat and you may learn something)
    
          Host *.kd.io
             User <username>
             ProxyCommand ssh %r@ssh.koding.com nc %h %p

How to figure stuff out
=======================
Lots of folks have been inspired to try linux, and/or software development because of Koding.  This is really fantastic.  I've gotten quite a bit of enjoyment (and employment) out of both over the last 20 years.  I love answering questions for folks largely because it helps me learn stuff and I enjoy helping people.  Not to mention, I remember being green as hell too.  

Why I'm writing this.  I'm seeing a ton of the same 10 questions or so posted to the activity stream. If you filter down to just status updates you'll see 2-5 posts on the top page.  If 1 or 2 of those posts are the same question that has been posted dozens of times, there's not much new visible content.  It becomes noise and obscures the meat.  This is death to online communities.  If all I'm getting is noise, I won't come back to dig for the meat.   The questions aren't bad.  The people asking aren't dumb. They're just from people who have never done this before.

So, in order to help new folks figure some stuff out on their own here's some pointers on finding your own answers, and how to ask questions.

- Want to know how to install yacc on your koding vm?  Well, your vm is running ubuntu, so you'd want to search for ['how do I install yacc on ubuntu'](http://lmgtfy.com/?q=how+do+I+install+yacc+on+ubuntu#)
- Some things are koding specific.  If the instructions for ubuntu don't work for you try [how do I ssh to my kodig vm](https://www.google.com/search?q=how+do+I+ssh+to+my+koding+vm&oq=how+do+I+ssh+to+my+koding+vm)
- If you're still completely stuck after googling around for a bit, by all means ask your question!  Provide some detail
- What you're trying to do  
    - What you've tried
    - Where you're stuck
    - What errors you're getting (cut and paste specific text if possible)
- This information does a few things.
    - It shows the person who might answer your question that you're willing to do some work.  You're not just asking because it's easier than looking it up yourself.
    - It adds some interest to the question.  Some of the details may point to new problems the solve.  Programmers and systems folks love solving problems.
    - It teaches you something.  The act of researching your problems is going to be used over and over again as you write your code/admin your boxes.  I constantly google for stuff when I'm working.  

Anyway, keep messing around, making mistakes, and fixing them.  The koding folks have provided a really neat set of tools with very easy recovery from mistakes.
