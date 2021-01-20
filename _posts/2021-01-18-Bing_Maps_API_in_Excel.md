"---
title: 'Bing Maps API in Excel'
layout: post
tags: []
category: 
Uncategoried
---

<p>I was tasked with building a carbon calculator for a conference. Delegates would enter their origin and the modes of transport. The system would then calculate the carbon cost and add it to a list. At the end of the conference we were going to sum up the carbon cost and offset it with tree planting. Covid put a stop to the conference which was a win in terms of carbon.</p>



<p>The easiest way I could think of creating this was in excel and luckily you can access the bing and google maps apis from within Excel to calculate the distances. Bing Maps ended up being used as you can use it for free without significant limits.</p>



<p><strong>Get an api key here</strong>: https://www.bingmapsportal.com/</p>



<p><strong>Generate Lat and Long for the origin and desitinations</strong>:</p>



<p>First enter the address details into empty cells. Then we use the api call    <strong>https://dev.virtualearth.net/REST/v1/Locations?countryRegion=$1&amp;adminDistrict=$2&amp;locality=$3&amp;postalCode=$4&amp;addressLine=$5&amp;maxResults=1&amp;o=xml&amp;key=$k</strong>    to return the Lat and Long values. Within the string we need to substitute $1, $2, $3, $4, $5 and $k for values. We do this with a substitute formula <strong>=SUBSTITUTE(SUBSTITUTE(SUBSTITUTE(SUBSTITUTE(SUBSTITUTE(SUBSTITUTE(point.url,""$1"",C$16),""$2"",C$15),""$3"",C$14),""$4"",C$13),""$5"",C$12),""$k"",bingmaps.key)</strong>. Then to return a result pass that line via the web service function <strong>=WEBSERVICE(C18)</strong>. The result us a very long string starting <strong>&lt;?xml</strong>. To filter out the information we need use <strong>=@FILTERXML(C20,""//Latitude[1]"")</strong> and <strong>=@FILTERXML(C20,""//Longitude[1]"")</strong>. The final result is four cells with the lat and long for the origin and destination.</p>



<p><strong>Calculate the travel distance between the two co-ordinates</strong>:</p>



<p>Similar to above we take an api call https://dev.virtualearth.net/REST/v1/Routes/DistanceMatrix?origins=$1&amp;destinations=$2&amp;travelMode=$3&amp;o=xml&amp;key=$k substitute in origin and destination co-orfinates, travel mode and api key. Call it with web service and filter out the travel distance component.</p>



<p>More info here: https://chandoo.org/wp/distance-between-places-excel-maps-api/</p>


<!-- wp:image {""id"":185,""sizeSlug"":""large""} -->
<figure class=""wp-block-image size-large""><img src=""https://gisdriverslicence.files.wordpress.com/2020/09/carbon-footprint-calculator.png?w=700"" alt="""" class=""wp-image-185"" /></figure>
<!-- /wp:image -->


<p>To clear the origin and destination address cells I assigned a macro to a button labelled clear.</p>


<!-- wp:coblocks/gallery-masonry {""align"":""wide"",""gridSize"":""lrg""} -->
<div class=""wp-block-coblocks-gallery-masonry alignwide""><div class=""coblocks-gallery has-caption-style-dark has-gutter""><ul class=""has-grid-lrg has-gutter-15 has-gutter-mobile-15""><li class=""coblocks-gallery--item""><figure class=""coblocks-gallery--figure""><img src=""https://gisdriverslicence.files.wordpress.com/2020/09/asign-macro-to-button-1.png?w=692"" alt="""" data-id=""180"" data-imglink="""" data-link=""https://gisdriverslicence.wordpress.com/asign-macro-to-button-1/"" class=""wp-image-180"" /></figure></li><li class=""coblocks-gallery--item""><figure class=""coblocks-gallery--figure""><img src=""https://gisdriverslicence.files.wordpress.com/2020/09/clear-cells-macro-1.png?w=237"" alt="""" data-id=""181"" data-imglink="""" data-link=""https://gisdriverslicence.wordpress.com/clear-cells-macro-1/"" class=""wp-image-181"" /></figure></li></ul></div></div>
<!-- /wp:coblocks/gallery-masonry -->


<p>To copy the delegate details and carbon calculations into a records tab I assigned another macro to a submit button.</p>


<!-- wp:coblocks/gallery-masonry {""align"":""wide"",""gridSize"":""lrg""} -->
<div class=""wp-block-coblocks-gallery-masonry alignwide""><div class=""coblocks-gallery has-caption-style-dark has-gutter""><ul class=""has-grid-lrg has-gutter-15 has-gutter-mobile-15""><li class=""coblocks-gallery--item""><figure class=""coblocks-gallery--figure""><img src=""https://gisdriverslicence.files.wordpress.com/2020/09/submit-details-to-list.png?w=700"" alt="""" data-id=""183"" data-imglink="""" class=""wp-image-183"" /></figure></li><li class=""coblocks-gallery--item""><figure class=""coblocks-gallery--figure""><img src=""https://gisdriverslicence.files.wordpress.com/2020/09/copy-to-record-sheet-macro.png?w=700"" alt="""" data-id=""184"" data-imglink="""" class=""wp-image-184"" /></figure></li></ul></div></div>
<!-- /wp:coblocks/gallery-masonry -->"
