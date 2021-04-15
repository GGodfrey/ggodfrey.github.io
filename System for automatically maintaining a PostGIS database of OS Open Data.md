---
created: 2021-04-15T12:41:06+01:00
modified: 2021-04-15T12:46:00+01:00
---

# System for automatically maintaining a PostGIS database of OS Open Data

OS open data is great

The downside is that you have to manually download each dataset, upload to PostGIS and then set up default styles. It's very time consuming. Ideally I would refresh all the data regularly but it's such a big job that I don't.

So the mission is to automate the whole system.

Download all data sets
Upload / overwrite to PostGIS database
Apply default styles

Optional extra: publish via mapserver for web apps


The solution .... I'm working on it.

The open data API should be able to handle the download

The upload would be some combination of GDAL and portion python

Applying the styles I have no idea