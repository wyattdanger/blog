---
layout: post
title: Scraping Open Graph Metadata With Node
date: 27/06/2011
comments: true
categories: [javascript, node, opengraph]
---
At [Converge SE](http://convergese.com/) this weekend, I had the opportunity to attend a workshop on programming social web applications taught by Principal Software Enginner at Yahoo, [Jonathan LeBlanc](http://www.jcleblanc.com/). 

One thing Jonathan covered was the [Open Graph Protocol](http://ogp.me/). Open Graph makes it easy for any developer to add metadata to their website pages. The data is primarily used control the title, description, image source, and URL to be displayed when their pages are shared on Facebook, but can be used by anybody.

<!-- more -->

Jonathan gave us a couple homework assignments during the presentation, one of which was to build an Open Graph metadata parser. Granted, Facebook already provides [one of these](https://developers.facebook.com/tools/lint/), but it proved to be a fun exercise in [Node.js](http://nodejs.org/). Using [Express](http://expressjs.com/) I was able to build the parser in half an hour and then deploy to Heroku's new [Cedar stack](http://devcenter.heroku.com/articles/cedar) in a few minutes.

The app grabs the URL passed to it, renders the DOM on the server, and extracts the needed meta tags. 

The [source](https://github.com/wyattdanger/og-lookup/) is available on Github and a [demo](http://og-quickcheck.herokuapp.com/) is live on Heroku. Go ahead, give it a shot! I recommend looking up [MailChimp](http://og-quickcheck.herokuapp.com/?url=http%3A%2F%2Fmailchimp.com).

