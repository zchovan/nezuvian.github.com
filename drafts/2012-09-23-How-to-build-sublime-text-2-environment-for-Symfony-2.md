---
layout: post
category: symfony
tags: [symfony, sublime text, php, coding]
---

I've been using PHPStorm for PHP development for a while and I liked it a lot, however since Symfony 2 came out coding became quite annoying due to the lack of autocompleting of routes, entity names, templates, etc... Writing these "by hand" without the good old friend <kbd>Ctrl</kbd>+<kbd>Space</kbd> made a lot of people frustrated.
Then came an [article](http://www.symfony-zone.com/wordpress/2011/11/07/how-to-build-a-great-eclipse-environment-for-symfony2-development/) about Eclipse solving pretty much every problem other IDEs had with Symfony 2.
My only problem was that I really don't like Eclipse :) Still I was patient because PHPStorm 5 was in EAP then and there were some talks about better Symfony support. Then PHPStorm 5 finally arrived! and the only thing I noticed was the new MVC panel which in my opinion wasn't even close to helping my daily work -_-" After this I thought this is gonna suck for a few months more, then one day guided by some random tought I opened a Symfony project in Sublime Text 2, opened a Controller, started to code something, accidentally hit <kbd>Ctrl</kbd>+<kbd>Space</kbd> and there it was, a working autocomplete for Symfony 2. After this I decided to take a better look on what exactly can be done with this "simple" text editor, this post is about what I found :)
<!-- more start -->

So the main task was turning a text editor into something that can do everything a full fledged PHP IDE and some more. I made a list what were the features I really needed or thought essential for a Symfony project, this might be a little subjective, but it goes something like this:

* real time code linting for php, js, css/sass/less, etc.
* easy file traversing eg. go to definition, go to file, etc.
* support for PHP namespaces
* Symfony CLI integration
* PHPUnit support
* phpDoc support
* customisable file templates
* code snippets
* twig support
* sass/less support
* git support
* (a solarized theme :) )

In a few days I was able to create a list of plugins that turn ST2 into something that is able to do all of these, so here are the list of the plugins:

* AdvancedNewFile
* CTags
* CTags for PHP
* FileTemplates
* Git
* JSLint
* Package Control
* PHP Namespace Command
* PHP-Twig
* Phpcs
* PhpDoc
* PhpDox
* PHPUnit
* Sass
* SideBarEnhancements
* SublimeLinter
* Symfony2 Snippets

All of these can be installed with Package Control, to avoid having to install them one by one you can edit your package control settings (read more about it [here](https://github.com/mrmartineau/SublimeTextSetup/issues/3)) and add all of them. I created a [gist](https://gist.github.com/3772713) so you just have to copy it.

[thx4tips](http://blog.stuartherbert.com/php/2012/02/28/setting-up-sublime-text-2-for-php-development/)
<!-- more end -->