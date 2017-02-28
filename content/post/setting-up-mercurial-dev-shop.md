+++
tags = ["mercurial","source control","development"]
categories = ["development","source control"]
date = "2011-04-20T00:00:00Z"
title = "Setting Up Mercurial Dev Shop"
keywords = ["development","mercurial","source control"]

+++

For a long time I have wanted to use a distributed source control management tool at work. I have looked at both Mercurial and Git and decided that I would like try Mercurial. So recently I have had the opportunity to use Mercurial on a new project.

<!--more-->

I have used Visual Source Safe briefly and have mostly used Subversion with TortoiseSVN. So I found it quite easy to switch to TortoiseHg. I am still getting to grips with Mercurial, but I have really enjoyed using it and think I will permanently move to using Mercurial.

Finally I wanted to setup a stable repository for the project so that I could push my changes to a Mercurial server and in the future setup cruise control to pull the changes from a central location. Also it would allow my manager to view the changes without having TortosieHg installed on his machine.

Since we are a Microsoft dev shop, I decided it would be easier to setup Mercurial on IIS. I found quite a few posts on setting up Mercurial on IIS 7, but had quite a difficult time getting it to work. I have also found differences in the setup process for Windows Server 2008 R2 (64 bit) and Windows Server 2008 (32 bit). So in this post I am going to list the blog articles that helped me to setup a Mercurial server successfully.

I started off by experimenting on a Windows Server 2008 (32 bit) VM (Virtual Machine). After many attempts I finally found a combination of two blogs post that helped me get Mercurial running.

* Jake Murzy’s Blog – Installing and Setting Up Mercurial on Windows/IIS7 running Python
* Matt Hawley – Setting up Mercurial server in IIS7 using a ISAPI module

> Note: I didn’t have a problem installing isapi-wsgi on the virtual machine since the virtual machine had the MSVCR71.dll file in the System32 folder.

VM Details: 32-bit Microsoft Windows Server 2008, 1GB RAM and 16GB HDD running on VMWare server.

The Virtual Machine also had the following software products installed:

* Mozilla Firefox/Chrome
* 7 zip
* Notepad++
* VM Ware tools
* IIS 7 with IIS 6 Management Compatibility and Application development services installed

After following the instructions from the two posts I got the Mercurial web interface working. However when I came to install it on a server running Windows 2008 R2 (64 bit), I couldn’t seem to get it to work. So after googling a bit I found the following post which helped me get Mercurial setup on my server.

Stacking Code – [Running a Mercurial Server on IIS 7.5](http://stackingcode.com/blog/2011/02/24/running-a-mercurial-server-on-iis-7-5-windows-server-2008-r2)

