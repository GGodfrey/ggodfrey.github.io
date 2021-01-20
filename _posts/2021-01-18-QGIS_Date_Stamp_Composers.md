"---
title: 'QGIS Date Stamp Composers'
layout: post
tags: []
category: 
Uncategoried
---

<p>I have a print composer that use regularly to create plans for engineers to print out and use on site. Lists of addresses get geocoded and then batches of sheets printed out using Atlas but thats another story. Why its not done on tablets is another story.</p>



<p>The composer has a date stamp which I had been manually updating, not even considering that this should be automated. Now it is using an expression in a text box.</p>


<!-- wp:image {""id"":413,""sizeSlug"":""large"",""linkDestination"":""media""} -->
<figure class=""wp-block-image size-large""><a href=""https://gisdriverslicence.files.wordpress.com/2020/10/image-16.png""><img src=""https://gisdriverslicence.files.wordpress.com/2020/10/image-16.png?w=1023"" alt="""" class=""wp-image-413"" /></a></figure>
<!-- /wp:image -->


<p>My first thought was this formula but it didn't seem to auto update:</p>



<p>              <strong>day_of_week(</strong> <em>now</em>() <strong>)</strong>    ||'-' ||   <strong>month(</strong> <em>now</em>() <strong>)</strong>   ||'-' ||   <strong>year(</strong> <em>now</em>() <strong>)</strong></p>



<p>The second iteration was: </p>



<p>               <strong>format_date</strong>(       <em>now</em>(),       'dd/MMM/yy'       )</p>



<p>The format can be altered as per the info provided on the right of the expression dialogue, although you seem limited to / as the delimiter.</p>


<!-- wp:image {""id"":411,""sizeSlug"":""large"",""linkDestination"":""media""} -->
<figure class=""wp-block-image size-large""><a href=""https://gisdriverslicence.files.wordpress.com/2020/10/image-15.png""><img src=""https://gisdriverslicence.files.wordpress.com/2020/10/image-15.png?w=1024"" alt="""" class=""wp-image-411"" /></a></figure>
<!-- /wp:image -->"
