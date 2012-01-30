---
layout: post
title: Responsive Enhancement
date: 2012-01-16 09:51
comments: true
categories: [css, buildconf, responsive design]
---

While in Belfast at [BuildConf](http://2011.buildconf.com), I attended a workshop on Responsive Enhancement taught by [Jeremy Keith](http://adactio.com). 

Forget what you know about web design. From now on, view web design as a union of [responsive design](http://www.alistapart.com/articles/responsive-web-design/) and [progressive enhancement](http://www.alistapart.com/articles/understandingprogressiveenhancement) with a ["mobile first"](http://www.lukew.com/ff/entry.asp?933) approach.

<!-- more -->

Remember that HTML is an inherently responsive medium, and that we web designers broke that once we applied a fixed width to a container element. In fact, the [first HTML document published to the Web](http://www.w3.org/History/19921103-hypertext/hypertext/WWW/TheProject.html) is responsive in the sense that it scales to whatever device you are using.

Don't make your web designs responsive, keep them responsive.

##### A Note on "Responsive"
Before we go on about what is "responsive", let's clarify that media queries are only one part of responsive design. 

- A flexible grid.
- Flexible images.
- Media queries.

<hr>

### The browser is always variable.

In the year 2000 in *[The Dao of Web Design](http://www.alistapart.com/articles/dao/)*, John Allsopp wrote:

> The web’s greatest strength, I believe, is often seen as a limitation, as a defect. It is the nature of the web to be flexible, and it should be our role as designers and developers to embrace this flexibility, and produce pages which, by being flexible, are accessible to all.

Consider the range of devices with a Web browser: desktops, laptops, netbooks, tablets, smart phones, e-book readers, video game platforms, ... the list goes on. Is your website built in such a way that it can be accessed from all devices? Do you build for the lowest common denominator and then enhance with layout and interactions? That's right, *layout is an enhancement.*

Furthermore, bandwidth on mobile devices is limited, 

> We should suggest design rather than control it.

#### Mobile First
You can't sprinkle media queries onto your existing website like magic dust. You have to shift thinking and design for mobile first. Start with a minimal mobile website and enhance it to the desktop experience.

#### Content First, Not Context First
Don't assume the user's context. Don't assume all mobile visitors only want to accomplish one specific task.

#### Speaking of Context
Design so that your users won't need to use [Instapaper](http://www.instapaper.com/) or  [other](http://www.readability.com/) [related](http://www.apple.com/mac/includes/builtin/safari_reader.html) [tools](http://readitlaterlist.com/) to comfortably read your page.

#### Overthought Navigation
Users goals are often overshadowed by bloated navigation. Consider the old school way of designing a web site, beginning with wireframes. The first thing designed is the header and navigation, exhaustively overdesigned and ....

![Bagcheck navigation screenshot](/images/bagcheck.png)

Content first, navigation second.

#### Alternative to wireframes: Style Tiles
Consider mood and branding, not layout. Style tiles are about organizing colors, typography, and the overall feel of a website design. Here are some examples from [Samantha Warren's fantastic write-up on style tiles](http://badassideas.com/style-tiles-as-a-web-design-process-tool/): 

![Style Tile 1](/images/styletile.jpg)

![Style Tile 2](/images/styletile-2.jpg)

These tiles offer two different designs for the same project, without the time-consuming full-page layout work or overthought navigation. The best part about style tiles is that *you can go straight from the style tile into the browser to start designing.*

#### Serving images responsively
https://github.com/filamentgroup/Responsive-Images
http://www.sencha.com/products/io/
http://adaptive-images.com/

http://fittextjs.com/ for full-width text on all devices.

