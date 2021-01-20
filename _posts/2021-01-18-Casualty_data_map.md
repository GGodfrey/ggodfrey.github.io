"---
title: 'Casualty data map'
layout: post
tags: []
category: 
Uncategoried
---
I was asked to create a 'casualties per km' map of the London road network, using Transport for London road casualty data. I had a spreadsheet with the values and a shapefile with the road network.

In both files there is a 'Node from' and a 'Node to' field, a node being a road junction, which describes the section of road network where there is data. Which allows a unique id to be created by concanternating them together. This unique id can be used to create a join between the spreadsheet and vector layer.

<a href=""https://gisdriverslicence.files.wordpress.com/2020/09/node.jpg""><img class=""alignnone size-medium wp-image-80"" src=""https://gisdriverslicence.files.wordpress.com/2020/09/node.jpg?w=300"" alt="""" width=""300"" height=""259"" /></a>

However to confuse the issue the vector layer was in smaller segments, split every time a side road intersected. So these sections need to be joined together. Then a single length can be calculated. This is acheived by dissolving by the unique id.

&nbsp;

<a href=""https://gisdriverslicence.files.wordpress.com/2020/09/dissolve.jpg""><img class=""alignnone size-medium wp-image-82"" src=""https://gisdriverslicence.files.wordpress.com/2020/09/dissolve.jpg?w=300"" alt="""" width=""300"" height=""216"" /></a>

Once disolved together a new field 'Km' is created and length calculated.

<em>Round ($length/1000, 1)</em>

Followed by a second value

CasualtiesPerKm

<em>Casulaties / Km</em>

<a href=""https://gisdriverslicence.files.wordpress.com/2020/09/length.jpg""><img class=""alignnone size-medium wp-image-86"" src=""https://gisdriverslicence.files.wordpress.com/2020/09/length.jpg?w=300"" alt="""" width=""300"" height=""212"" /></a>"
