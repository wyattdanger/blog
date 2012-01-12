---
layout: post
title: Organizing Page Specific JavaScript
date: 22/08/2011
comments: true
categories: [javascript, jquery]
---

I often find myself repeating a JavaScript pattern, where I check for a DOM node&rsquo;s existence and fire a function if it&rsquo;s found. This weekend I put together a tiny jQuery plugin to abstract this pattern away into a more concise, readable format.

<!-- more -->

### Big Poppa

Big Poppa ([Github](https://github.com/wyattdanger/Big-Poppa)) aims to simplify this pattern and make page specific JavaScript management a bit easier.

<noscript>[Example](https://gist.github.com/1163371)</noscript>
<script src="https://gist.github.com/1163371.js"> </script>

In each example, Poppa checks for the DOM nodes specified in the key, and passes the matching nodes into the callback function, only if the key was found in the DOM.

Poppa also looks pretty clean in [CoffeeScript](http://jashkenas.github.com/coffee-script/).
<noscript>[Example](https://gist.github.com/1163444.js)</noscript>
<script src="https://gist.github.com/1163444.js"> </script>

Big Poppa is tiny (< 0.2K minified) and available on [Github](https://github.com/wyattdanger/Big-Poppa). 
