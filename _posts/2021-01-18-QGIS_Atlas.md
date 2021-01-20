"---
title: 'QGIS Atlas'
layout: post
tags: []
category: 
Uncategoried
---
The QGIS Atlas function will print multiple maps using the same print layout. Each separate map view is defined by a polygon in the 'coverage layer.

When coverage areas are adjacent and not regular shapes, you can get a situation where you print a map tile and items from other areas are visible across the boundary.

To solve this it is possible to use rule based symbology to style features based upon which coverage layer polygon is currently the @atlas_feature, which is generating the map tile.

<strong>Option 1</strong>: Make the coverage layer visible to act as a mask, then set the active @atlas_feature to be invisible. Use the expression below:

<em>$id = @atlas_featureid</em>

<strong>Option 2:</strong> Make only features which intersect with the @atlas_feature coverage layer polygon visible.

Set the points to be visible with this expression and toggle the other layers off.

<em>intersects( $geometry, @atlas_geometry )</em>

<a href=""https://gisdriverslicence.files.wordpress.com/2020/09/atlas.png""><img class=""alignnone size-medium wp-image-68"" src=""https://gisdriverslicence.files.wordpress.com/2020/09/atlas.png?w=300"" alt="""" width=""300"" height=""74"" /></a>

Note: All items will be visible until the Preview Atlas button is selected.

To change the @atlas_feature right click the coverage layer and set the feature as the atlas feature.

<a href=""https://gisdriverslicence.files.wordpress.com/2020/09/atlas-select.png""><img class=""alignnone size-medium wp-image-69"" src=""https://gisdriverslicence.files.wordpress.com/2020/09/atlas-select.png?w=300"" alt="""" width=""300"" height=""33"" /></a>

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;"
