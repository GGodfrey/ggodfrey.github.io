"---
title: 'QGIS Snapping lines to a base layer'
layout: post
tags: []
category: 
Uncategoried
---
The below image shows data collected using GPS survey kit. The dashed lines are double yellow lines collected during a survey. I wanted them to neatly follow the highway kerb lines show on the OS base mapping. They also need to be offset by a uniform 0.3 metres.

Use the 'snap geometries to layer' function first. Choosing the survey lines as the 'Input layer' and the base mapping as the 'reference layer'. The behaviour is 'Prefer closest point, insert extra vertices where required'. You can iterate over the layer using different behaviours to get the right effect.

Then style the snapped lines with a 0.3m offset. If the lines offset on the wrong side of the road then use the 'reverse' tool to change the line direction, the line will then offset in the opposite direction.

<a href=""https://gisdriverslicence.files.wordpress.com/2020/09/snapping.jpg""><img class=""alignnone size-medium wp-image-60"" src=""https://gisdriverslicence.files.wordpress.com/2020/09/snapping.jpg?w=300"" alt="""" width=""300"" height=""96"" /></a>"
