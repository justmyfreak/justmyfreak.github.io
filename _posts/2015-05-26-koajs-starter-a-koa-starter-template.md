---
layout: post
title: "koa-starter, a Koa starting template"
description: "koa-starter is a starting template for Koa"
category: 
- web dev
- nodejs
tags: []
permalink: koa-starter-a-koa-starting-template

share: true
comments: true
---

# What is koa-starter?
> [koa-starter](https://github.com/justmyfreak/koa-starter) is a Koa starting template which aims to give a minimal structure to Koa application. 

# koa-starter features

- Routing
- Controller
- View engine
- App Configuration
- Sample test using mocha

# Getting started 

#### Clone koa-starter:

{% highlight bash %}
$ git clone https://github.com/justmyfreak/koa-starter.git
{% endhighlight %}

#### Install dependencies:

{% highlight bash %}
$ npm install
{% endhighlight %}

#### Run koa-starter:

{% highlight bash %}
$ npm start
{% endhighlight %}

or 

{% highlight bash %}
$ node --harmony index.js
{% endhighlight %}

Open [http://localhost:3000](http://localhost:3000)

#### Run the test:

{% highlight bash %}
$ npm test
{% endhighlight %}

# Creating new controller

#### Create new controller inside `app/controllers/user.js`

{% highlight javascript %}
module.exports = {
    index: function *(next) {
        this.body = "User index";
    },
	
    view: function *(next, username) {
        this.body = "View user with username : "+this.params.username;
    }
};
{% endhighlight %}

#### Open `app/routes/index.js` and add newly created controller bellow indexCtrl

{% highlight javascript %}
module.exports = function(app) {
    var Router 	    = require('koa-router'), 
        indexCtrl   = require('../controllers/index'),
        viewCtrl    = require('../controllers/user');

        var router = new Router();
{% endhighlight %}

#### Define new endpoint

{% highlight javascript %}
router
    .get('/users', viewCtrl.index)
    .get('/user/:username', viewCtrl.view);

{% endhighlight %}

#### Open [http://localhost:3000/users](http://localhost:3000/users)

#### Open [http://localhost:3000/user/myusername](http://localhost:3000/user/myusername)