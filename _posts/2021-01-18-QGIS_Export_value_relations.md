"---
title: 'QGIS Export value relations'
layout: post
tags: []
category: 
Uncategoried
---

<p><strong>Problem</strong>: How to export a layer and retain values created with a value relations and lookup tables, rather than the underlying raw data.</p>



<p>I have a line layer (postgis) showing parking bays with road, restriction and times. Like this:</p>


<!-- wp:image {""id"":359,""sizeSlug"":""large"",""linkDestination"":""media""} -->
<figure class=""wp-block-image size-large""><a href=""https://gisdriverslicence.files.wordpress.com/2020/10/image-6.png""><img src=""https://gisdriverslicence.files.wordpress.com/2020/10/image-6.png?w=1010"" alt="""" class=""wp-image-359"" /></a></figure>
<!-- /wp:image -->


<p>All very neat but when I export to a CSV / spreadsheet it turns into a mess like this:</p>


<!-- wp:image {""id"":361,""sizeSlug"":""large"",""linkDestination"":""media""} -->
<figure class=""wp-block-image size-large""><a href=""https://gisdriverslicence.files.wordpress.com/2020/10/image-7.png""><img src=""https://gisdriverslicence.files.wordpress.com/2020/10/image-7.png?w=1024"" alt="""" class=""wp-image-361"" /></a></figure>
<!-- /wp:image -->


<p>The reason being is twofold. Firstly I have <a href=""https://gis.stackexchange.com/questions/240258/qgis-changing-the-attribute-input-fields-order/348160#348160"">hidden all the columns</a> not useful to the user, when they open the attribute table and reordered those that are.</p>


<!-- wp:image {""id"":363,""sizeSlug"":""large"",""linkDestination"":""media""} -->
<figure class=""wp-block-image size-large""><a href=""https://gisdriverslicence.files.wordpress.com/2020/10/image-8.png""><img src=""https://gisdriverslicence.files.wordpress.com/2020/10/image-8.png?w=249"" alt="""" class=""wp-image-363"" /></a></figure>
<!-- /wp:image -->


<p>Secondly, many of the fields are populated by drop down menus. The values in these are populated from a lookup tables, via a value relation widget. The result is that the user sees a text string but a single number is added to the table. There are <a href=""https://dba.stackexchange.com/questions/1910/why-use-an-int-as-a-lookup-tables-primary-key"">good database design reasons</a> for doing this but equally it does cause this issue.</p>



<p><strong>Solution</strong>: The solution is to tick “Replace all selected raw fields by displayed values” when exporting the file. This can be found within 'Select fields to export and their export option'. This also allows you to fine tune the fields you export and their display options.</p>


<!-- wp:image {""id"":357,""sizeSlug"":""large"",""linkDestination"":""media""} -->
<figure class=""wp-block-image size-large""><a href=""https://gisdriverslicence.files.wordpress.com/2020/10/image-5.png""><img src=""https://gisdriverslicence.files.wordpress.com/2020/10/image-5.png?w=594"" alt="""" class=""wp-image-357"" /></a></figure>
<!-- /wp:image -->"
