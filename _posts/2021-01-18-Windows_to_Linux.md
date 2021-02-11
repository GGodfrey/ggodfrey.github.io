---
modified: 2021-02-11T13:54:21+00:00
---

---
title: 'Windows to Linux'
layout: post
tags: []
category: 
Uncategoried
---

<p>My personal laptop was bought just after I graduated in 2012. As a result its showing its age and struggling with the basic day to day tasks. So I was looking for ways to speed it up. In addittion, many higher level GIS tasks use the Lixux terminal, or are at least described in tutorials from this perspective.  So with these two motivations I decided to set up a dual boot linux install where I am able to choose between windows and linux, to test out the idea.</p>



<p>This proved to be more difficult than expected. Linux just has a much higher learning curve than windows, it expects you to work allot more out. I probably could have got there faster but I was being careful not to damage my existing windows set up and the data on the harddrive. As it turns out I destroyed the windows set up somehow but luckily retained the data.</p>



<p>Below are a few pointers from my experience:</p>



<p>Distributons: Windows is a single product, if you want to install it you go straight to the windows download page. Linux however is a whole world of variants all built from a common core. So task one is to choose a distribution from the hundreds available. I chose Ubuntu as its the most high profile and apparently fairly user friendly. https://www.techradar.com/uk/best/best-linux-distros</p>



<p>Then you select the flavour of Ubuntu, these are different 'desktop environments' which change  the appearance and the software which it comes with as standard. I was looking for something that runs well on my old under powered laptop. Xubuntu seems to be the happy middle ground between speed and a modernish look and feel. https://itsfoss.com/which-ubuntu-install/ </p>



<p>Then we move to the install, instructions here: https://www.lifewire.com/guide-to-installing-xubuntu-linux-2202075. In summary:</p>



<p>download xubuntu.iso   https://xubuntu.org/download/</p>



<p>download rufus software, this installs the 'installer' onto a usb stick</p>



<p>Plug in usb, restart computer and straight away press F12 (or the equivalent on your machine) to open the boot loader menu. </p>



<p>Select the USB, likely at the bottom of the list</p>



<p>Next you will get options to try or install Xubuntu. The try option runs the operating system directly from USB stick, when you turn off everything returns to normal.</p>



<p>To install you need to consider partitions. Partitions are segments of your hard drive which behave as seperate drives. You will likely have a main partition and then another for your windows backup. There could be several more. You can create a new partition for Xubuntu by 'shrinking' the existing partition and using some of the empty space for a new partition. It is recomended you do this in advance using the windows tools.You need to consider the format and potentially seperate small partitions for swap and boot. This bit was frankly beyond me and I left allot to chance. Shrinking my main partition down to make room for a new 100GB partitition for Xubuntu. It seems 30Gb is the recomended minimum.</p>



<p>The installer asks you if you want to erase the disk (destroy your windows data) or something else. You get a simple looking slider which suggests you can shrink the windows partition to make space for a new Xubuntu install. However its all a bit vague and I was worried about it damaging my data. So I went for the advanced options. Selected my new partition and then was faced with a drop down for 'device for boot loader installation'. Some research shows this is basically the files the computer looks for at startup. Where to put it has some debate online. It seems for Windows10 era laptops its actually irrelevent but will likely use the top /sda option which I think is kind of the parent level to the child partitions below it.</p>



<p>https://www.lifewire.com/guide-to-installing-xubuntu-linux-2202075</p>


<!-- wp:image -->
<figure class=""wp-block-image""><img src=""https://www.lifewire.com/thmb/S3ilXk9wrVntPtcY6CMxIcCGd9I=/1024x768/filters:no_upscale():max_bytes(150000):strip_icc():format(webp)/xubuntu-custom-partition-fcf597a2f05a44019923dd9235f53b78.jpg"" alt=""Xubuntu custom partition"" /></figure>
<!-- /wp:image -->


<p>So far the results are good, its clean, simple, and much faster. I can still access my old data. The appearance is a bit clunky but that was the trade off for speed.The downside is in an initial test where I just ran Xubuntu without installing, Windows got corrupted. I'll reinstall at some point but for now its fine. Basic tasks also can take a bit of googling such as installing Zoom and Chrome. However I think its an ok learning curve. The key difference is that using the terminal is the default method for everything and the graphical interface is secondary.</p>
"