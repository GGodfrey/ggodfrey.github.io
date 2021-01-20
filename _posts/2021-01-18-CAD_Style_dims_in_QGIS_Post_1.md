"---
title: 'CAD Style dims in QGIS Post 1'
layout: post
tags: []
category: 
Uncategoried
---

<p>In the world of AutoCAD, dimensions are fully built in and work really well. Whereas in QGIS there is no built in function to create them.</p>



<p>However, it is possible to set up line styles to emulate them. </p>



<p>There are a few options; a separate layer dedicated to dims, a separate line style within a layer containing the objects you want to measure or build the dimension into the line style so that every object has a dim automatically generated.</p>



<p>In my case I settled with option 2. I have a layer containing parking restrictions, with styles linked to a 'type' drop down menu. Draw a line and select the 'Dim' type and it is styled as a dim.</p>



<p>I ended up with two variants, standard and offset. The offset version stops the dim obscuring the underling object. The red dotted line doesn't appear on screen but represents the geometry of the item which is invisible.</p>



<p>{comparison image]</p>



<p>The style has a few components:</p>



<p>The central line: This runs the length of the line</p>



<p>End bars</p>



<p>Arrows</p>



<p>Measurement: This is a label, set to be positioned in the middle of the geometry and offset to match the central line. It used the formula   <em>round( $length II 'm' , 2) </em>  to dynamically generate the value. I then expanded this out to allow this value to be manually over ridden. Say the line is 9.99metres long, you don't need that level of accuracy and 10m would be neater. Enter 10m in the label field and the expanded formula overides the origional formula.</p>



<p><span class=""has-inline-color has-vivid-cyan-blue-color"">CASE WHERE   <em>""Label"" IS NULL </em>  THEN   <em>round( $length II 'm' , 2)</em>   ELSE   <em>""Label""</em>   END</span></p>



<p></p>



<p>Units of measurement:</p>
"
