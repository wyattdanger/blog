---
layout: post
title: "Keeping Track of Media Queries"
date: 2012-03-31 11:17
comments: true
categories: [css, sass, responsive design]
---

When building a responsive design, it can be helpful to have a reminder of which media query is currently in effect. It's easy to use CSS generated content to display the current query. 

<!-- more -->

{% gist 2265989 %}

The [above snippet](https://gist.github.com/2265989) is in SASS, and is also [available](https://gist.github.com/2266035) in CSS.

#### Demo

[Here is a demo](/which-media-query-demo/)

#### Mobile First

It should be noted that the above queries work around a mobile-first approach. It assumes that your base styles will be written for mobile devices, and that you'll progressively enhance from there, remembering that [layout is an enhancement](/2012/02/01/responsive-enhancement).
