---
layout: post
title: Blogging with Jekyll
description: blogging with jekyll and getting it running on github pages
comments: true
share: true
---

# What is Jekyll?
> Transform your plain text into static websites and blogs. Simple, static, and blog-aware

Jekyll let us write our blog in plain text. No, we are not gonna write post in plain HTML. We write content using [markdown](http://daringfireball.net/projects/markdown/). Jekyll will do its magic to convert plain text to static HTML.

# Why do we need Jekyll?
It's a common question. We already have powerful blogging and content management system such as Wordpress, Drupal, Joomla, etc. My personal answer is **Simplicity**. I love Jekyll's no-database approach. Serving static pages means, faster load time.

### Simple
No database setup, comment meoderation, no annoying update notification. Jekyll focus on content. 

### Static
Write content on static markdown, textile, or liquid. Jekyll will '*compile*' it to html static site. Serving static file is a lot faster than serving content from database.

### Blog-aware
Jekyll owns permalinks, categories, pages, posts, and custom layouts. Don't worry, you cand extends Jekyll's ability with plugin.

# Installing and Running Jekyll

Installation process is a bit intimidating if we never use terminal or command prompt. I assume you are using Mac or Linux and have Ruby installed on your computer. All you need to do is just open your terminal and write following commands : 

{% highlight bash %}
$ gem install jekyll
$ jekyll new my-awesome-site
$ cd my-awesome-site
$ jekyll serve
{% endhighlight %}
	
now open [http://localhost:4000](http://localhost:4000). Your Jekyll powered site is ready. 

# Where to write?
You may be wondering where to login and manage your site. You will never find it on Jekyll. all you need to do to write content or post is just browse your `_posts` directory. You'll find `*.md` file, just create new `.md` file or copy + paste existing file and rename it. Close your Jekyll server by using `ctrl+c` in your terminal and run `jekyll serve` again to restart your Jekyll server.

# Jekyll + Github = <3
You maybe wondering how to make Jekyll site online. Do I have to upload it to my shared hosting? No, we can't upload it on shared hosting. All you need to have is just GitHub account. All you need to do is just register on [GitHub](http://github.com) if you don't have an account. Then follow these steps :

- Create repository named `username.github.io` where `username` is your registered username
- You will be given how-to guide after repository creation
- Push your Jekyll site to github 
- Your site is available on username.github.io
- Github host your site for **FREE** :)

**PS : You must have experience with Git before deployin on GitHub**