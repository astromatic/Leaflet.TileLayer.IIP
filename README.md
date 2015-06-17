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

Note: `L.tileLayer.iip` is equivalent to `new L.TileLayer.IIP`

### `L.TileLayer.IIP` options 

`L.TileLayer.IIP` supports all options from the regular `L.TileLayer` plus:

* `contrast` : Contrast fractor. Default is 1.0.
* `gamma` : Display gamma. Default is `1.0` for 8 or 16 bit images, and `2.2` for 32 bit (integer or floating-point) images.
* `cMap` : Colormap for single-channel images. Valid colormaps are `'grey'`, `'jet'`, `'cold'` and `'hot'`. Default is `'grey'`.
* `invertCMap` : Invert Colormap (like a negative). Default is `false`.
* `quality` : JPEG encoding quality in percent. Default is `90`.
* `mix`: Switch on multi-channel mixing. Default is `false`.
* `mixingMatrix`: 2D array containing the mixing matrix. Default is `[[1,0,0],[0,1,0],[0,0,1]]`.
* `channelLabels`: Array of strings containing the channel labels. Default is `['Channel #1', 'Channel #2', ...]`
* `minMaxValues`: 2D array of min and max values for each channel. Default is the set of values returned as Min-Max-sample-values by IIPImage (which correspond to the values stored as TIFF SMinSampleValue and SMaxSampleValue tags).

[Leaflet]:http://leafletjs.com
[IIP]:http://iipimage.sourceforge.net
[demo]:http://image.iap.fr/iip
