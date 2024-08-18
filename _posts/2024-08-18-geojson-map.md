---
layout: post
title: a post with geojson
date: 2024-08-18 17:57:00
description: A map to celebrate our website opening
tags: formatting charts maps
categories: sample-posts
map: true
---

This is an example post with some [geojson](https://geojson.org/) code. The support is provided thanks to [Leaflet](https://leafletjs.com/). To create your own visualization, go to [geojson.io](https://geojson.io/).

````markdown
```geojson
{
  "type": "FeatureCollection",
  "features": [
    {
      "type": "Feature",
      "properties": {},
      "geometry": {
        "coordinates": [
          [   175.49684695569000,
              -40.35740380000000
          ]
        ],
        "type": "Point"
      }
    }
  ]
}
```
````

Which generates:

```geojson
{
  "type": "FeatureCollection",
  "features": [
    {
      "type": "Feature",
      "properties": {},
      "geometry": {
        "coordinates": [
          [    175.49684695569000,
              -40.35740380000000
          ]
        ],
        "type": "Point"
      }
    }
  ]
}
```
