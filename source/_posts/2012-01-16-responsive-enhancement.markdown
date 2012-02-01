---
layout: post
title: Responsive Enhancement
date: 2012-01-16 09:51
comments: true
categories: [css, buildconf, responsive design]
---

While in Belfast at [BuildConf](http://2011.buildconf.com), I attended a workshop taught by [Jeremy Keith](http://adactio.com). 

Forget what you know about web design. From now on, view web design as a union of [responsive design](http://www.alistapart.com/articles/responsive-web-design/) and [progressive enhancement](http://www.alistapart.com/articles/understandingprogressiveenhancement) with a [mobile first](http://www.lukew.com/ff/entry.asp?933) approach. We'll call this "responsive enhancement."

<!-- more -->

Remember that HTML is an inherently responsive medium, and that we web designers broke that once we applied a fixed width to a container element. In fact, the [first HTML document published to the Web](http://www.w3.org/History/19921103-hypertext/hypertext/WWW/TheProject.html) is responsive in the sense that it scales to whatever device you are using.

Don't make your web designs responsive, keep them responsive.

### Problems With the Old Way
Consider the old school way of designing a web site, beginning with wireframes. A page is filled with gray boxes, and most content is absent. Navigation is designed in the wireframing stages, often exhaustively overdesigned. The design is framed within a fixed width container, geared for viewing on laptop and desktop computers.

Up until recently it was widely accepted that a website would conform to a set width (960px is a popular example) and not much thought, if any, was given to mobile traffic. Fluid width layouts were possible, but less common. Designers like the control offered by a fixed width layout, but designing for a fixed width layout is much more like designing for print than for the web.

### The browser is always variable.

In the year 2000 in *[The Dao of Web Design](http://www.alistapart.com/articles/dao/)*, John Allsopp wrote:

> The web’s greatest strength, I believe, is often seen as a limitation, as a defect. It is the nature of the web to be flexible, and it should be our role as designers and developers to embrace this flexibility, and produce pages which, by being flexible, are accessible to all.

Viewport, bandwidth, and context are always unknowns. Consider the range of devices with a web browser: desktops, laptops, netbooks, tablets, smart phones, e-book readers, video game platforms... the list continues. Is your website built in such a way that it can be accessed from all devices? Do you build for the lowest common denominator and then enhance with layout and interactions? That's right, *layout is an enhancement.* Does your layout improve the users experience or detract from it? Does it adapt to the users needs?


#### Mobile First
You can't sprinkle media queries onto your existing website like magic dust. You have to shift thinking and design for mobile first. You must stop designing from some imaginary page in, and instead design from your content out. Designing for mobile first helps you focus on the essentials and remove the cruft. Start with a minimal mobile website and enhance it to the desktop experience.

The idea that a mobile visitor only wants to quickly accomplish one specific task [is a myth](http://adactio.com/journal/4443/). Don't assume the user's context. They may be hurriedly looking for contact information, or they may be casually browsing. Responsive design can help serve layout optimized for variable viewports, and it can help preserve bandwidth, but it does not solve problems of user context. 

#### Speaking of Context
Web content is no longer confined to web pages. People can [snip up your content](http://www.alistapart.com/articles/orbital-content/) for reading on their own devices with tools like [Instapaper](http://www.instapaper.com/) and [Readability](http://www.readability.com/). The success of such tools is an indicator that web designers miss the mark, and users see the designs as obstacles rather than enhancements. Design your pages in such a way that visitors won't feel compelled to read them elsewhere. By designing in a mobile first way, you can cut down on the clutter and distractions that cause users to leave your site in the first place.

#### Alternative to Wireframes: Style Tiles
Style tiles are about organizing colors, typography, and the overall feel of a website design. They let the designer consider mood and branding without worrying about layout. Here are some examples from [Samantha Warren's fantastic write-up on style tiles](http://badassideas.com/style-tiles-as-a-web-design-process-tool/): 

![Style Tile 1](/images/styletile.jpg)

![Style Tile 2](/images/styletile-2.jpg)

These tiles offer two different designs for the same project, without the time-consuming full-page layout work or overthought navigation. The best part about style tiles is that *you can go straight from the style tile into the browser to start designing.*


#### Serving images responsively
To effectively adapt to variable devices, consider serving images responsively. Bandwidth on mobile devices is limited, and you can improve your page load time by serving images catered to the user's device. By combining JavaScript with server-side directives (think htaccess or nginx.conf) you can serve appropriately sized images programmatically. 

The Filament group has a Github repository for serving resonsive images at [https://github.com/filamentgroup/Responsive-Images](https://github.com/filamentgroup/Responsive-Images).

### Not in Kansas Anymore
The way people access the Internet is changing, and by adopting a mobile first approach to design and practicing responsive enhancement you can help your content reach a broader range of users. Designing for a fixed-width page is an increasingly poor decision, instead embrace the inherent flexibility of the web. We should suggest design rather than control it.
