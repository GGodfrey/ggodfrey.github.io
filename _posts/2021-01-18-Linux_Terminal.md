"---
title: 'Linux Terminal'
layout: post
tags: []
category: 
Uncategoried
---

<p>Setting up Xubuntu has involved allot of use of the 'terminal' like the Windows command line but way more integrated into the everyday experience. Especially for installing software.</p>



<p>Ctlr+Alt+T to open it</p>



<p>Then types a command, or more likely copy and paste from a website tutorial or forum. Copy is CTRL+SHIFT+C, paste is CTRL+SHIFT+V. Then press enter to execute it. It feels very opaque as nothing much happens. For example you can create a new folder using command ""mk TEST"", and there is no indication in the terminal that it worked despite the folder called test appearing in unless you type an actual command.</p>



<p>In the example below I create a new folder and a new file. As per this introductory tutorial: https://maker.pro/linux/tutorial/basic-linux-commands-for-beginners</p>


<!-- wp:image {""id"":509,""sizeSlug"":""large"",""linkDestination"":""media""} -->
<figure class=""wp-block-image size-large""><a href=""https://gisdriverslicence.files.wordpress.com/2021/01/image.png""><img src=""https://gisdriverslicence.files.wordpress.com/2021/01/image.png?w=1024"" alt="""" class=""wp-image-509"" /></a></figure>
<!-- /wp:image -->


<p>The key use of the terminal seems to be to instahis and configure software. This is often a quick option compared with the graphical way for common software like Chrome. For more complex software like GeoServer or PostgresSQL database it becomes integral to the process.</p>



<p>The sudo command refers to acting as super user, apt is application and install installs. I got stumped by entering the password, nothing happens. Turns out passwords are hidden, you type, press enter and hope for the best.</p>



<p>There is the idea of repositories, lists of software available for download and install.</p>


<!-- wp:syntaxhighlighter/code -->
<pre class=""wp-block-syntaxhighlighter-code""># Download software
$ wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
# Install
$ sudo apt install ./google-chrome-stable_current_amd64.deb
# Open
$ google-chrome</pre>
<!-- /wp:syntaxhighlighter/code -->


<p></p>
"
