---
layout: post
title: "Tools for Modern Web Developer"
modified: 2014-06-03 15:46:09 +0700
tags: [web dev, tools]
comments: true
share: true

published: true
---

Development tools are created not only to boost developer's productivity, but also make development process more enjoyable. In this article, I will cover some development tools that I used often. Please note that I won't cover in-depth tutorial for each tools. This article covers only a gentle intruduction, reason to use, and main function of the tools.

# Git
[Git](http://git-scm.com/) is distributed source code management originally created by Linus Torvalds. Being distributed means that Git repository is not centralized. Each repository has its own history and full tracking capabilities. Each repository can be synched to fetch or push changes. Git popularity is increasing due to social coding service like GitHub.

In the past, I often made backup folder to create source code version. But the problem is the more version I create, it takes more space on my disk. I couldn't see the difference between one version to other in details. By using Git, I can track my repository changes and give version to my source code. Git repository takes less space on disk, because it save only code changes not whole repository. I can compare each file to see the difference.

<figure class="center">
	<a href="{{ site.url }}/images/posts/tools-for-modern-developers/nogit-git-comparison.png"><img src="{{ site.url }}/images/posts/tools-for-modern-developers/nogit-git-comparison.png" alt="Git comparison"></a>
	<figcaption>Versioning without Git and using Git comparasion</figcaption>
</figure>

To start using git, you can refer to [https://help.github.com/articles/set-up-git](https://help.github.com/articles/set-up-git). GitHub has a [nice interactive tutorial](http://try.github.com/) to learn about Git.  If you don't like to use ```terminal```(*nix, OSX) or ```cmd```(windows), you can use GUI program such as [SourceTree](http://www.sourcetreeapp.com/), [SmartGit](http://www.syntevo.com/smartgithg/), or [others](http://git-scm.com/downloads/guis). But I suggest you to use ```terminal``` since it will be handy and save you a lot of time.

Git is useful not only to give version and track code changes, but also make collaborative development easier. Team members can work together and review the code. Sayanee has great example how to do team collaboration using Git and GitHub on [tutsplus](http://code.tutsplus.com/articles/team-collaboration-with-github--net-29876)

# Node.JS
Node.JS is a software platform for server-side and networking applications. Node.JS are written in JavaScript and run on Google V8. Nowaday, Node.JS is not only used as server-side and networking applications but also to do general purpose scripting. You can think Node.JS gives JavaScript capabilities to be general purpose programming language such as Ruby, Java, and Python. In this article, we are not going to explore how to use Node.JS to build server side application. We will cover how to utilize Node.JS power to boost developer productivity.

Node.JS has its own dependancy manager named Node Packaged Modules (NPM). NPM is like Gem to Ruby and Pear/Composer to PHP. Dependancy manager allows us to include others code easily. You can browse packages on [npmjs](https://npmjs.org/).

To start using Node.JS, you can download it on [http://nodejs.org/download/](http://nodejs.org/download/). Choose your machine platform. To test your installation, you can run ```node -v```. If you see version number, it means Node.JS is intalled into your machine.

# Yeoman
[Yeoman](http://yeoman.io/) is a great tool to scaffold modern web apps. It helps you by generating your web apps project, testing your project, and deploying your project. Yeoman uses Bower and Grunt to provide good workflow.

Installing Yeoman is easy if you have Node.JS installed on your machine. Open your ```terminal``` or ```cmd``` and run ```npm install -g yo``` (you may need ```sudo``` access to do it). Check your installation by using ```yo -v``` command. If it shows version number, you are ready to rock. 

The next step is to generate your project. Yeoman provides a lot of [generator](http://yeoman.io/community-generators.html). We will be using ```webapp``` generator. Install webapp generator by running ```npm install -g generator-webapp``` then create your project by using ```yo webapp```. You will be prompted to choose some options, just choose according to your need. Project generation will take some times depending on your connection. After  installation has been completed, run ```grunt serve```. Your application will be opened on browser at http://localhost:9000

What was just happened? You may be wondering how is everything working. As I mentioned that Yeoman use Bower and Grunt to provide a good workflow. You just use ```grunt serve``` to run your web apps. Yeoman generator provide some grunt tasks such as ```grunt serve``` and ```grunt build```. 

# Bower
[Bower](http://bower.io/) is a package manager for the web created by Twitter folks. Bower solves problem about JS and CSS library dependancy. In old days, we should include jQuery library manually when working with jQuery UI. By using bower, we just add jQuery UI using simple commands and its dependancy will be automatically included. We don't need to add JS or CSS to HTML manually, bower and grunt will handle this for you.

Installing Bower is easy, open terminal and run ```npm install -g bower```. You will need Git installed to make Bower working properly. If you follow this article from beginning, Bower will be installed automatically when your run ```npm install -g generator-webapp```. Change your directory to newly created Yeoman project and run ```bower install jquery```. jQuery will be added to your project. 

Bower uses ```bower.json``` to list your project JS and CSS dependancy. To install dependancies on your ```bower.json``` simply run ```bower install``` and all dependancies will be downloaded and installed to your project. You can search packages registered to Bower by running ```bower search [<name>]```

<figure>
{% highlight json %}
{
	"name": "yo",
	"private": true,
	"dependencies": {
		"bootstrap": "~3.0.3",
		"jquery": "~1.11.0"
  	},
  	"devDependencies": {}
}
{% endhighlight %}
	<figcaption class="center">bower.json example</figcaption>
</figure>

# Grunt Task Runner
[Grunt](http://gruntjs.com) is JavaScript task runner. Task runner means automation. Grunt help you to eleminate repeteative tasks such as minification, compilation, unit testing, linting, and much more. All we need to do is just configure the tasks on `Gruntfile.js` then we can run tasks such as `grunt build` to build your project (minifying, linting, etc) or `grunt test` to run unit testing.

Grunt can be installed by running `npm install -g grunt-cli` from cmd or terminal. `grunt-cli` allows you to run `grunt` command from your terminal. Grunt can be run from anywhere as long as `Gruntfile.js` exist in your project. Try running `grunt` commant to your webaapp project. You will see bunch of text displayed after each task has been completed or error has been occured.

Grunt provides plugins to aid you doing repetitive task. Plugin listing can be found at [http://gruntjs.com/plugins](http://gruntjs.com/plugins). 

# Conclusion

<figure class="center">
	<a href="{{ site.url }}/images/posts/tools-for-modern-developers/yeoman-grunt-bower-love.png"><img src="{{ site.url }}/images/posts/tools-for-modern-developers/yeoman-grunt-bower-love.png" alt="Yeoman + Grunt + Bower = Love"></a>
	<figcaption>Yeoman + Grunt + Bower = Love</figcaption>
</figure>

Yeoman give a better and fun workflow by utilizing Grunt and Bower. Removing repetitive task boredom and making JS-CSS addition easier. 

<figure class="center">
	<a href="{{ site.url }}/images/posts/tools-for-modern-developers/yeoman-webapp-directory.png"><img src="{{ site.url }}/images/posts/tools-for-modern-developers/yeoman-webapp-directory.png" alt="Yeoman webapp project directory"></a>
	<figcaption>Yeoman webapp project directory</figcaption>
</figure>

As you can see, yeoman creates `bower.json` for Bower dependancues and `Gruntfile.js` for Grunt configuration. Your application is located on `/app`. You will see there is `bower_components` folder. `bower_components` will hold all library of your bower depandancy.

Yeoman can be used not only for front-end web development, but also for back-end. [generator laravel](https://www.npmjs.org/package/generator-laravel) is an example of Yeoman usage with back-end web development. 