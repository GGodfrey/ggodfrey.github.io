---
title: 'GitHub Pages, Jekyl and Markdown'
layout: post
tags: []
category: Uncategoried
---
I was looking for a simple way to host webmaps for my blog, which was just a basic free wordpress page. I didn't have anywhere to host the individual html, geoJSON and other files that make up a webmap.

Paying for hosting for such a small ammount of data seemed a step too far as well. Then once I started thinking about it I wondered whether just a simple HTML page was enough for my basic blog as well.

The point I ended up at was to use GitHub as my hosting platform. Using the standard GitHub repositories to save the files and the GitHub Pages function to create a website using html saved in the repository.

Then on top of this I discovered Jekyl which is a basic html blog programme which works from GitHub Pages. I forked Jekyl Now, adjusted a few basic configurations and away I went.

Initially I thought I would have to manually edit the blog posts in a text editor on my laptop, then commit them to GitHub. Using the GitHub desktop tool. 

However there is a better solution. The Jekyll Editor Chrome extension allows you to make posts in an interactive editor, not dissimilar to the old basic wordpress editor. Then commit them to your GitHub repository / website.

It's pretty good. The online downside is that if you want images then you need to manually upload them to github, copy the url and paste that into the editor.

If I was doing just a blog then wordpress was fine. I had a nice template and the ability to copy and paste in images is great. However for my niche case where I wanted to save files for web maps and GIS then this is a nice system.

There appear to be lots of nice, high quality templates but when I try to fork them they don't work. I think there are addittional steps that need to be taken but I'm yet to understand it.