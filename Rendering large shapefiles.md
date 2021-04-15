---
created: 2021-04-15T12:35:29+01:00
modified: 2021-04-15T12:40:12+01:00
---

# Rendering large shapefiles

I have a shapefile with OS master map for the whole of a London borough. 150Mb which is almost unusable when trying to open it across my companies VPN whilst working at home.


I only needed a small area so I did the following.

Toggle off rendering
Create a temp polygon layer
Draw a polygon over the area of interest plus a buffer
Use extract by location to save only the polygons from the OS the intersects the temp layer.
Took less than 10 seconds to create a new temp layer with just the area I needed
Turned rendering back on


Ideally it would all be loaded to postgis and run effecient but until that later is loaded then this was the fastest solution. I could then work easily with no lag.