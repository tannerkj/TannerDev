---
layout: post
title:  "A Brief Look At Vector Tiles"
date:   2015-03-15
categories: vector_tiles formats
author: Joshua Tanner
---

#A Brief Look at Vector Tiles - Part I

This post is a very 'basic' look into vector tiles.  Feel free to make improvements to this post through [github](https://github.com/tannerjt/blog_posts/blob/master/vector_tiles.md).  Also, please use the links throughout this document to understand more about vector tiles. 

At ESRI's 2015 Developer Conference, the plan to [implement vector tiles](http://video.esri.com/watch/4215/smart-mapping-with-vector-map-tiles) into their mapping platform was announced.  Most traditional GIS analysts and developers have created [tile caches](http://resources.arcgis.com/en/help/main/10.2/index.html#//001700000189000000) or [consumed tiled map service layers](https://developers.arcgis.com/javascript/jsapi/arcgistiledmapservicelayer-amd.html) to implement complex geometries with [more efficiency](http://www.usgs.gov/faq/categories/9860/3604) as part of their business processes.  To most of the industry (I'm assuming), [vector tiles](http://wiki.openstreetmap.org/wiki/Vector_tiles) is a new concept that offers many advantages over traditional formats.  Although the concept is similar to raster tiles, vector tiles return the actual features which creates the ability to manipulate the style and symbology of features dynamically.  This can be done, all while benefiting from the efficiency of only needing to load tiles within the current extent and not the entirety of a features geometry and attributes.  Also, vector tiles also benefit over feature services because the geometry is essentially cached and not needed to be dynamically created on the server in most cases.

It is important to know that although vector tiles are new to Esri's platform, they are already present in the geospatial community elsewhere.  [Mapbox](https://www.mapbox.com/)  has [developed a standard for an open source vector tile format](https://www.mapbox.com/blog/vector-tiles/) and uses it at the core of [tilemill](https://www.mapbox.com/tilemill/).  In fact, [Esri has adopted](https://www.mapbox.com/blog/vector-tile-adoption/) this specification in it's implementation of vector tiles.  If you look at the vector tile spec defined by mapbox, you will also see various [applications and tools that implement it](https://github.com/mapbox/vector-tile-spec/wiki/Implementations).

Within [Esri's current JavaScript API](https://developers.arcgis.com/javascript/jsapi/), I don't see support for vector tiles but I'm sure the next release will include it.  OpenLayers  does support [a TileVector](http://openlayers.org/en/v3.3.0/apidoc/ol.source.TileVector.html) format, as illustrated in [this example](http://openlayers.org/en/v3.3.0/examples/tile-vector.html).

There are various tile-generation libraries available for creating vector tiles, and according to Esri's announcement, a toolbox will be available directly though their Desktop (or Pro) software.  One nice example I found was created by [Glob3 Mobile](https://github.com/glob3mobile) called [mmt-vector-tiles](https://github.com/glob3mobile/mmt-vector-tiles) which can generate vector tiles directly from a PostGIS database.  They also have a [good example](http://wb.glob3mobile.com/vl/index_lux.html) posted of this in action with OpenLayers 3.  If you look at the [file stucture](http://igosoftware.dyndns.org:8000/vectorial/lux_buildings_LEVELS_12-18_MERCATOR/GEOJSON/) of their tiles, it looks similar to what is shown in [Esri's presentation](http://video.esri.com/watch/4215/smart-mapping-with-vector-map-tiles) although I'm not certain it adheres to the same specification.

I've labeled this post 'Part I', as I'd like to dive deeper into the specification and illustrate different workflows to creating and consuming vector tiles.  If you haven't heard of vector tiles before, I hope this post has been useful.  More to come!

