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

# Getting Started

Starting new Koa app is pretty simple

### 1. Create new directory 

{% highlight bash %}
$ mkdir koa-sample
$ cd koa-sample
{% endhighlight %}

### 2. Create blank package.json and add Koa

{% highlight bash %}
$ echo '{}' >> package.json 
$ npm i koa --save
{% endhighlight %}

### 3. Create new ```app.js``` and paste following code :

{% highlight javascript %}
var koa = require('koa');
var app = koa();

app.use(function *(){
  this.body = 'Hello World';
});

app.listen(3000);
{% endhighlight %}

### 4. Run the app and open [http://localhost:3000](http://localhost:3000)

{% highlight bash %}
$ node --harmony app.js
{% endhighlight %}

# Next learning resources

For the next lesson, we will be creating Koa boilerplate to make development process easier.
Stay tune :) 