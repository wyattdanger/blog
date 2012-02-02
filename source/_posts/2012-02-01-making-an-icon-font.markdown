---
layout: post
title: "Making an Icon Font"
date: 2012-02-01 22:22
comments: true
categories: [svg, frontend]
---

While working on some fun stuff [at work](http://mailchimp.com/b/), I found myself needing to make a sprite full of 50+ icons. Designer [Aaron Robbs](https://twitter.com/#!/aaronrobbs) and I have been wanting to make an icon font for a while now (think [Pictos](http://pictos.cc/)), and I realized that instead of sprites, and icon font might be a better tool for the job at hand. 

<!-- more -->

A Google search led me to [Inkscape](http://inkscape.org/), which allows me to create an SVG font. Then I can convert the SVG font to TTF through [an online service](http://onlinefontconverter.com/), and then use [FontSquirrel](http://www.fontsquirrel.com/fontface/generator)'s `@font-face` generator to get all the formats I'll need for web embedding.

##### Why an icon font?

Icon fonts have excellent browser support (all the way back to IE4), they can be styled with CSS, their styles can be changed on CSS events, they don't pixelate, and they're easy to adjust (sure beats resizing a sprite and modifying the accompanying CSS!)

Depending on how many characters you include they can be very small in size, potentially smaller than all the icons you'd otherwise need to transfer over the wire.

If you're still not sold, check out [Chris Coyier's "Icon Fonts are Awesome" page](http://css-tricks.com/examples/IconFont/).

##### Building the font

Armed with my [collection of icons](http://dribbble.com/shots/232417-MailChimp-icon-set) in an Adobe Illustrator file and Inkscape, I began the tedious process of creating the font. Each icon needed to be saved as an SVG file, imported into Inkscape, properly resized and positioned on the artboard, run through a specific set of transforms, and then bound to a key. For more on the process, reference [this article](http://www.webdesignerdepot.com/2012/01/how-to-make-your-own-icon-webfont/) and [this video](http://www.youtube.com/watch?feature=player_embedded&v=_KX-e6sijGE#!).


![In progress](/images/inkscape.png)

##### Adding the font

Once all the characters are bound to keys, run through the conversion process mentioned before. To get the font into the page, use the `@font-face` syntax and then add the characters with CSS generated content to avoid polluting your markup. 

{% gist 1721329 %}

Note that you can also add the icons with the HTML5 `data` attribute.

{% gist 1721458 %}

Which will result in something like this:

![Example](/images/icon-font-example.png)


#####  Lesson Learned
Icon fonts are awesome. Currently the woff, ttf, and eot files are each under 20K, which is comparable to an optimized transparent png of 20px sprites. If you want an icon font but don't want to build one yourself, Pictos now offers [Pictos Server](http://pictos.cc/server), which allows you to build your own icon fonts from over 650 pre-made icon choices. Also, if you didn't look at [Chris Coyier's demo page](http://css-tricks.com/examples/IconFont/) earlier, be sure to give it a look.
 
