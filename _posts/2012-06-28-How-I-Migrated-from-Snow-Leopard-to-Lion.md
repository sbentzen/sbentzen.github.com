---
layout: post
published: true
tags:
- Interesting
- Lion
---

So this post will explain how I managed to upgrade from Mac OS X 10.6 Server to Lion Server. (this is kind of like an instructional mixed with what I was thinking at the time)

##Preparation##

1. As always, the first and most important step is to back up your entire drive. To do this, I used [Carbon Copy Cloner](http://www.bombich.com) and copied it over to an external drive.  
2. The next step was to export the service settings. To do this, you open Server Admin, click server and then export and service settings. It's the best idea to save this to your external drive as well.
3. Now we will export the directory data (skip this step if the server is bound to another directory). Open Server Admin and navigate to the Open Directory service. Select the archive pane and then select browse on the "archive location" button. It's best to navigate to the external disk you still have plugged in.
4. Now we download the Lion Installer application. You do know how to download it right?
5. Wait for it to finish downloading. Maybe if you have spare time, make another clone of your hard disk on another external drive or something? Never hurt to have more than one backup. :)
6. Here comes the fun part. I burned the installesd.dmg (in /Applications/Install Mac OS X Lion.app/contents/SharedSupport/) to a disk just in case. Now, go ahead and double click that installer.
7. This is where you wait for it to prepare the install.

##Installation##
8. The computer will reboot into the installer.
9. Follow the steps as prescribed and it will pretty much install by itself.
10. First things first, set the hostname, IP address, that junk.
11. Go to server admin and then restore your OD archive.

###This is where things went different for me###
Seeing as I previously had data I had to migrate that and get all of the settings working appropriately.  
12. I had to use some of the MigrationExtras (located at /System/Library/ServerSetup/MigrationExtras/) to migrate settings. (the mail data migration tool is in /usr/libexec/dovecot/).
13. __MAKE SURE YOUR CERTIFICATES ARE ALL PROPERLY SET FOR ALL SERVICES IN SERVER.APP__
14. move all websites into appropriately named folders in /Library/Server/Web/Data/Sites/CustomSitesDefault/ and then appropriately create the websites in Server.app
15. Finish setting up other services as required.

##NOTES:##
1. DO NOT MESS WITH RUBY (if you want wiki or profile manager services, there may be other services that rely on it.) [relevant article](http://support.apple.com/kb/TS4042?viewlocale=en_US&locale=en_US)
2. DO NOT ENABLE RAID ON THE ONSET OF INSTALL, it borks all things so bad that it just doesn't work, don't cause yourself the headache. I don't remember what I did to get it working, but I found an informative post [here](https://discussions.apple.com/thread/3197548) (scroll until you find tommiemel)
3. Things were different for me because I tried to upgrade From Snow Leopard with a software raid and preserve that raid into lion. Didn't work out so well… managed to get everything back up and running. But I pulled a mistake in doing what I said not to in #1.
