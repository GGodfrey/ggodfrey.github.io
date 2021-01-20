"---
title: 'CAD Style dims in QGIS Post 2'
layout: post
tags: []
category: 
Uncategoried
---

<p>Following on from my first post on creating CAD style 'dims' in QGIS.</p>



<p>How to adjust the dim so that it appears as two lines with a space for the number?</p>


<!-- wp:image {""id"":426,""sizeSlug"":""large"",""linkDestination"":""media""} -->
<figure class=""wp-block-image size-large""><a href=""https://gisdriverslicence.files.wordpress.com/2020/11/image.png""><img src=""https://gisdriverslicence.files.wordpress.com/2020/11/image.png?w=349"" alt="""" class=""wp-image-426"" /></a></figure>
<!-- /wp:image -->


<p>rather than a single line </p>


<!-- wp:image {""id"":428,""sizeSlug"":""large"",""linkDestination"":""media""} -->
<figure class=""wp-block-image size-large""><a href=""https://gisdriverslicence.files.wordpress.com/2020/11/image-1.png""><img src=""https://gisdriverslicence.files.wordpress.com/2020/11/image-1.png?w=305"" alt="""" class=""wp-image-428"" /></a></figure>
<!-- /wp:image -->


<p>The solution is to use a 'simple line' with a custom dash pattern, combined with a user defined formula.</p>



<p>The custom dash pattern takes a value formatted like this <em>4;5;5</em> , with each number representing a distance; alternating dash then gap. </p>



<p>The expression used has three segments, the first is half the length of the line minus 0.5 metres, then a gap of 1 metre and then again half the length of the line minus 0.5 metres.</p>



<p>(( $length /2) -0.5) || ';1;' || (( $length /2) -0.5)</p>


<!-- wp:image {""id"":431,""sizeSlug"":""large"",""linkDestination"":""media""} -->
<figure class=""wp-block-image size-large""><a href=""https://gisdriverslicence.files.wordpress.com/2020/11/image-3.png""><img src=""https://gisdriverslicence.files.wordpress.com/2020/11/image-3.png?w=1024"" alt="""" class=""wp-image-431"" /></a></figure>
<!-- /wp:image -->


<p>Previously I had used a double headed arrow style for the line. This wouldn't accept a dash pattern so I changed tack and used a simple line combined with triangular marker symbols, placed at the end of the lines and rotated to look like arrow heads.</p>



<p>The result looks like this:</p>


<!-- wp:image {""id"":429,""sizeSlug"":""large"",""linkDestination"":""media""} -->
<figure class=""wp-block-image size-large""><a href=""https://gisdriverslicence.files.wordpress.com/2020/11/image-2.png""><img src=""https://gisdriverslicence.files.wordpress.com/2020/11/image-2.png?w=620"" alt="""" class=""wp-image-429"" /></a></figure>
<!-- /wp:image -->"
