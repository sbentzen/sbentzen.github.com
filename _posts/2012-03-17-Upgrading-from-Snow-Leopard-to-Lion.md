---
layout: post
published: true
tags:
- INTERESTING
---
This post chronicles the journey that I had while upgrading from Snow Leopard Server to Lion Server. Short Story: it was a pain in the butt for most of it.

##Saturday##

6:00 -- Having issues downloading the server components and it won't install because of that? maybe I'll burn a dvd if I have to.

7:00 -- Unfortunately the beginning of the lion upgrade isn't going as peachy as I would have wanted, need to do some crazy stuff to get the darn thing to work. No idea what's completely wrong with it at the moment.

8:40 -- this has to be the worst upgrade I have ever experienced, it's not even done and I had to make a DVD to install :(

9:22 -- an even bigger pain in the butt than I thought, going to try to wipe and install like new. Big pain in the butt if that's what it takes

9:30 -- and I have to set up from new... Bollocks

11:03 -- install failed, apparently it doesn't like software raid in any way shape or form for boot disks, apple I am disappoint.

11:36 -- This has become a total pain in the butt… I had never expected an install to be this much of a drag. I'm making some tea to calm myself down from this whole thing… maybe I'll be able to get it installed if I break the raid, restore to snow leopard and upgrade from there?

Midnight -- Holy shit, guess what decides that it wants to actually begin properly installing? This is just madness… so much so that I have inserted an appropriate image.

![Sparta](http://images4.wikia.nocookie.net/__cb20111122193821/sonic/images/9/90/Madness-this-is-sparta.jpg)
> Madness… this is sparta!  
> -- King Leonidus

##Sunday##

11:45 -- Alright, well, I forgot to put some stuff in here, but I managed to restore the OpenDirectory Master and now I just have to restore every other service that I have and then move it behind an airport base station. Sounds easy enough right?

2:30 -- Alright, Things are going very well, I'm getting new services set up and all things haven't imploded or exploded. It looks like my pain has ended for now.

4:00 -- and the pain has returned, i should have known better than to update rubygems, and thanks to this [article](support.apple.com/kb/TS4042?locale=en) but did I think otherwise

6:46 -- I think things are going well. I just need to completely check the split DNS and get the rest of the zones that way to resolve properly, I feel like I have the patience of a deity right now.

10:44 -- alright, well after an entire weekend it looks to be done, just waiting on DNS to settle down and hopefully everything is up on the awww right. I hope to do a full write-up of this experience some time soon, maybe post it in a seperate page or something. Had to call up my ISP at least twice today to get them to clear the arp cache, pretty darn good support.