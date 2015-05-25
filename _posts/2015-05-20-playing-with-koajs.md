---
layout: post
title: "Playing with Koa : Introduction"
modified: 2015-05-20 16:48:52 +0700
tags: [web dev, javascript, nodejs]
category:
- web
- nodejs

share: true
comments: true

permalink: playing-with-koa-introduction
---

# What is Koa?
> Koa, next generation web framework for Node.js

Koa is a new web framework which aims to be smaller, more expressive, and more robust foundation building web applications and APIs.

# Why koajs?

It's a common question. We have a lot of Node.js frameworks and one of them is Express which is very mature and widely used. I personally hate Node.js because of its callback. When writting large scale Node.js application we are going to have a lot off callbacks stacked. It's so refershing to use Koa. Simply because Koa leverage generator which allows developer to ditch callbacks and improve error handling.

# Installation

Koa requires Node 0.11.x for the ```--harmony``` flag which enable ES6's generators to the app.

{% highlight bash %}
$ node --harmony my-koa-app.js
{% endhighlight %}

