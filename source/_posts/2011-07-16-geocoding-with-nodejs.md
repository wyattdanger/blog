---
layout: post
title: Geocoding With Node.js
date: 16/07/2011
comments: true
categories: [javascript, jquery]
---
Need to make an asynchronous call to Google's geocoding or reverse geocoding service in a Node.js application?  The [Geocoder module](https://github.com/wyattdanger/geocoder) makes it simple to fetch geocoordinates based on street addresses, or to fetch localities based on LatLng pairs. 

<!-- more -->

Adding the module to your project is easy, it is available as a [npm package](http://search.npmjs.org/#/geocoder). Just `npm install geocoder`. After requiring the module, it exposes two methods: `geocode` and `reverseGeocode`. 

`geocode` requires two arguments: a location in the form of a String, and a callback function which will accept the geodata returned from Google. The geodata will look like [this](http://code.google.com/apis/maps/documentation/geocoding/#JSON).

`reverseGeocode` requires three arguments: a latitude, longitude, and callback function.

Both methods accept an optional last argument, an options Object which can pass along other Google API parameters, such as `sensor`, which defaults to false.

<script src="https://gist.github.com/1086532.js" > </script>

Of course, feel free to [fork it on Github](https://github.com/wyattdanger/geocoder)!
