"---
title: 'GeoPackage Lockfiles'
layout: post
tags: []
category: 
Uncategoried
---

<p>I was trying to copy a GeoPackage from one place to another. I discovered there were two extra files with the same name as the Geopackage but different extensions .gpkg-wal and .gpkg-shm.</p>



<p>My worry was that moving these files could corrupt the data so I did a little research. I discovered that when QGIS is connected to a .gpkg, any edits are recorded to the .gpkg-wal and .gpkg-shm files. When the session ends the temp files are committed to the main file.</p>



<p>A session is not just the time the layers are edited (yellow pencil toggled on) but the whole time QGIS is open.</p>



<p>There is a way to turn off this functionality but it might cause issues when two actions are carried out on the file simultaneously. I see no reason why I would need to meddle.</p>



<p>There is very in depth discussion on stack exchange: https://gis.stackexchange.com/questions/224188/geopackage-error-is-mounted-and-in-wal-mode-this-combination-is-not-allowed</p>
"
