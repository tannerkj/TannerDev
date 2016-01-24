---
layout: post
title:  "A Quick Look At Aurelia"
date:   2016-01-23
categories: aurelia javascript
author: Joshua Tanner
---

I have been a big proponent of AngularJS.  My biggest compaint with any framework however, is the learning curve compared to just jumping into coding with no new *stuff* to learn.  I spent years working with Angular, but I am always suprised at how quickly I forget the ins and outs of new language or framework.  Now that I'm preparing to work on a new project, I tried to go back to Angular docs to freshen up.  AngularJS 2.0 is out, which means more things to learn and test out.  Learning is never a bad thing, but re-learning can get tedious and sometimes counterproductive.  I know JavaScript like the back of my hand, shouldn't a framework feel the same?

At last, a quick browse around the web led me to discover [Aurelia].  It's new ([although this is relative](http://www.isaacchansky.me/days-since-last-new-js-framework/)), but already it is up to a production ready Beta 1 release.  It is built using modern ECMAScript 2016 and follows similar concepts we use in all modern MV* frameworks.  Data binding, dependency injection, templating, routing, etc.  

The best thing I noticed so far is that the framework is very discreet.  There aren't many 'frameworky' things to learn and lets you leverage the power of a framework without needing to be intimate with the framework.  If you've spent hours re-learning backbone, AngularJS, React, etc... you know what I mean.  

I feel like the Aurelia framework should follow Douglas Crockfords convention of: **AngularJS 2.0 - The Good Parts** by **Rob Eisenberg** (the creator of Aurelia).  In fact, it turns out [Rob Eisenberg](https://github.com/EisenbergEffect) is actually the driving input behind Angular 2.0 and now known as [the guy who left Angular](http://eisenbergeffect.bluespire.com/leaving-angular/).  

[Aurelia]: http://aurelia.io/docs.html#/aurelia/framework/1.0.0-beta.1.0.8/doc/article/what-is-aurelia

**Getting Started**

The [Getting Started Guide](http://aurelia.io/docs.html#/aurelia/framework/1.0.0-beta.1.0.8/doc/article/what-is-aurelia) on Aurelia provides a straight forward approach to getting introduced to the framework.  Different paths are avaialbe depending on what type of background you are coming from. You can follow along with their [getting started guide](http://aurelia.io/docs.html#/aurelia/framework/1.0.0-beta.1.0.8/doc/article/getting-started) on your own using either the ES 2016 or Typescript kit.

I'm using a [simple web server](https://www.npmjs.com/package/http-server) to serve out the web files, since Aurelia is simply client side libraries.  This is also referenced in the guide:

```
npm install http-server -g
http-server -o
```

The -o flag will open your app in a browser.  You should see a comforting 'Welcome to Aurelia' string in your browser.

I also suggest watching [Rob's video introducing Aurelia](https://vimeo.com/131641012).  The video intoduces the framework in a very straightforward, digestable manner.  I think this was the point, as is the point of the framework itself.

**Final Thoughts**

I've spent the better part the last day building some sample apps with Aurelia... and I have to say I'm impressed.  This should be my primary framework for the coming year.
