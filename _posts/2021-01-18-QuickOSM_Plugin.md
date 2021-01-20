"---
title: 'QuickOSM Plugin'
layout: post
tags: []
category: 
Uncategoried
---

<p>Summary: QGIS plugin to download features from open street map.</p>



<p>The task was to provide bus routes and schools data for a London Borough, to use within a project. My first thoughts were OS Open Data local for the schools and London data store for the bus routes. </p>



<p>A quick option was to use Open Street Map data for both. The advantage of this approach is that I can quickly download to memory layers the specific types of features I want, just for the area needed. The downside is that the data might not be accurate. I've certainly found in the past that the schools layer isn't perfect. Bus stops change over time and are more complex so might be off.</p>



<p> This can be achieved using the Quick OSM plugin in QGIS, which allows you to query the Overpass API website and download the results straight to QGIS memory layers.</p>


<!-- wp:image {""id"":527,""sizeSlug"":""large"",""linkDestination"":""media""} -->
<figure class=""wp-block-image size-large""><a href=""https://gisdriverslicence.files.wordpress.com/2021/01/image-3.png""><img src=""https://gisdriverslicence.files.wordpress.com/2021/01/image-3.png?w=1024"" alt="""" class=""wp-image-527"" /></a></figure>
<!-- /wp:image -->


<p>Working out the correct tags to use is a bit hit and miss.  The quick query option provides drop down menus but there are loads of options. The quick The<a href=""https://wiki.openstreetmap.org/wiki/Map_features#Route""> OSM website</a> has all tags listed. The extents can be limited using place names or layer extents in QGIS.</p>


<!-- wp:image {""id"":523,""sizeSlug"":""large"",""linkDestination"":""media""} -->
<figure class=""wp-block-image size-large""><a href=""https://wiki.openstreetmap.org/wiki/Map_features#Route""><img src=""https://gisdriverslicence.files.wordpress.com/2021/01/image-1.png?w=616"" alt="""" class=""wp-image-523"" /></a></figure>
<!-- /wp:image -->


<p>For complex queries you write a kind of code / query syntax.</p>


<!-- wp:image {""id"":525,""sizeSlug"":""large"",""linkDestination"":""media""} -->
<figure class=""wp-block-image size-large""><a href=""https://gisdriverslicence.files.wordpress.com/2021/01/image-2.png""><img src=""https://gisdriverslicence.files.wordpress.com/2021/01/image-2.png?w=1024"" alt="""" class=""wp-image-525"" /></a></figure>
<!-- /wp:image -->"
