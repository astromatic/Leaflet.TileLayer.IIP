Leaflet.TileLayer.IIP
===================
This plugin adds [IIP][] layering support to the [Leaflet][] library.

### Requirements
* Leaflet 0.8 or newer

### Demo
See [demo][]

### Usage

```html
<html>
 <head>
  <link rel="stylesheet" href="Leaflet/dist/leaflet.css" />
  <script src="Leaflet/dist/leaflet-src.js"></script>
  <script src="Leaflet.TileLayer.IIP/TileLayer.IIP.js"></script>
 </head>
 <body>
  <div id="map" style="height:256px"></div>
  <script>
   var map = L.map('map', {center: [0.0,0.0], zoom: 0}),
       layer = L.tileLayer.iip('/fcgi-bin/iipsrv.fcgi?FIF=/path/to/image.ptif').addTo(map);
  </script>
 </body>
</html>
```

[Leaflet]:http://leafletjs.com
[IIP]:http://iipimage.sourceforge.net
[demo]:http://image.iap.fr/test
