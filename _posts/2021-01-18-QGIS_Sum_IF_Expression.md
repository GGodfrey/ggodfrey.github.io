"---
title: 'QGIS Sum IF Expression'
layout: post
tags: []
category: 
Uncategoried
---
The equivalent of the Excel SumIF function in QGIS is the sum function. It's syntax is <em>sum(expression[,group_by][,filter]).</em>

In the example below the 'Sum' column is a virtual field populated with the following fomula.         <em>sum(""Price"", ""Type"", ""Type""='Cheap')</em>

Sum together the values in the 'price' column, for each unique value in the 'Type' column. As we ran this on an entire column then you get lots of duplicate values, for every instance that the same criteria are met.

<a href=""https://gisdriverslicence.files.wordpress.com/2020/09/sum-function-table.png""><img class=""alignnone size-medium wp-image-29"" src=""https://gisdriverslicence.files.wordpress.com/2020/09/sum-function-table.png?w=300"" alt="""" width=""300"" height=""196"" /></a>

If we only want to return a single value for a specfic attribute then we add an extra 'filter' term to the expression. e.g. <em>sum(""Price"", ""Type"", ""Type""='Cheap')     </em>which outputs 5.

&nbsp;

&nbsp;"
