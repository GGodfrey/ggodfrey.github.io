---
title: 'AUTOCAD Calculate total length of lines'
layout: post
tags: []
category: Uncategoried
---




<p><a href=""https://forums.autodesk.com/t5/autocad-forum/how-to-calculate-the-total-length-of-multiple-lines/td-p/5120514""><strong>TLEN LISP routine:</strong></a></p>



<p>AutoCAD doesn't have anything like that built in, but it's easily done with TLEN.lsp (Total LENgth of selected objects)</p>



<p>http://www.turvill.com/t2/free_stuff/tlen.lsp</p>



<p>If you're not familiar with how to use lisp, simply copy/paste (CTRL+V)&nbsp;<strong>ALL</strong>&nbsp;the text and characters in the above link into your command line and press Enter, then type TLEN into the command line and follow the command prompt (select the objects)&nbsp; Note using this method, the lisp is only loaded for the current session, if you want it to be a permanent feature, Add it to the Startup Suite or the acaddoc.lsp file.</p>



<p><strong>Export to QGIS: </strong></p>



<p>QGIS is a good option if using AutoCAD LT where LISP doesn't work or if you want to see a spreadsheet to view more detail. In QGIS you can view an attribute table that shows which layer the features are from.</p>


<!-- wp:list -->
<ul><li>Save the drawing or part of as a .dxf</li><li>Open in QGIS</li><li>Use field calculator to add a virtual field and populate each row with $length</li><li>Open the statistics panel to view the total length of all features or of all selected features</li><li>For example select all features from a CAD layer using the LAYERS attribute</li><li>For more detail such as summing the length for each layer; save as a spreadsheet and then open in Excel</li></ul>
<!-- /wp:list -->


<p></p>
"
