"---
title: 'Roads within an area'
layout: post
tags: []
category: 
Uncategoried
---

<p>A council was operating a number of controlled parking zones. I was asked to compile a list of each area and the names of the roads which fell within the areas. This became the record of which roads were eligable for which permits.</p>



<p>The solution was as follows:</p>


<!-- wp:list {""ordered"":true} -->
<ol><li>Load a polygon layer showing the areas and the OS Open Roads layer for the road network. Delete the private road catagory as wouldn't be eligable.</li><li>Create a name attribute and populate for each polygon.</li><li>Use the Intersection tool to clip the road network to the polygon boundaries and create a seperate road network for each areato the area boundaries.</li><li>Use the 'Join attributes by location' tool to append the polygon area name to the roads.</li><li>Export as a csv and open in Excel.</li></ol>
<!-- /wp:list -->

<!-- wp:image {""id"":209,""sizeSlug"":""large""} -->
<figure class=""wp-block-image size-large""><img src=""https://gisdriverslicence.files.wordpress.com/2020/09/join-by-attri.jpg?w=856"" alt="""" class=""wp-image-209"" /></figure>
<!-- /wp:image -->"
