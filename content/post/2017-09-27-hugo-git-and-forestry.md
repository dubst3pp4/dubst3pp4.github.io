---
categories:
- website
date: 2017-09-27 22:57:56 +0200
tags:
- Hugo
- Forestry
- Github
title: Hugo, GitHub and forestry.io

---
To set up my personal Github pages, I decided to use a static site stack - sometimes called the [JAMStack](https://jamstack.org/best-practices).

The idea is, instead of using a huge and slow CMS like WordPress or Drupal, to build a whole site of only static HTML and asset files. Neither the dynamic, server side rendering of the pages, nor a database is required.<!--more-->

You simply put your content as Markdown files into a tree structure, which represents your site structure and the static site generator turns it into a bunch of HTML files which you can upload to your server.

For the generation of the site I'm using [Hugo](https://gohugo.io), a site generator which is written in Go and is available for Linux, Windows and MacOS.

Hugo allows you to setup a complete website just with some commands, a little configuration file and your content files written in Markdown. Although it has an extensive documentation, it is sometimes hard to find the information you are looking for due to the huge amount of possibilities on how to use Hugo.

The benefit of using a site generator is, that you can work with your familar Git workflow. Whether you're trying out a new feature or whether you want to revert to an older state of the site, Git allows you to do so!

Another great feature of using Git is that it allows you to write your content offline. You can simply push your changes to the deployment environment when you're connected to the internet again.

[forestry.io](https://forestry.io) sits on top of such a site generator like Hugo and provides to you or even your team a graphical user interface like a traditional CMS does. Although you don't need a GUI to run Hugo, it is a very handy way to edit your content for example from your mobile phone (like I'm doing now) as it features a content editor with WYSIWYG preview, a simplified process of publishing your changes and much more. In contrast to Hugo itself, which runs on your local development machine, forestry.io is a hosted webservice which is free for personal use.

But why [GitHub](https://github.com)? One reason is that I'm using GitHub as a remote repository for Hugos source files (the markdown and the configuration of this site). And with the help of forestry.io it is really easy to deploy the generated files directly to a branch, which in turn is connected to my GitHub page.

The source of this site for example is stored in the branch [src](https://github.com/dubst3pp4/dubst3pp4.github.io/tree/src?files=1) of my repository, while the HTML files of my site are then generated into the [master](https://github.com/dubst3pp4/dubst3pp4.github.io/tree/master?files=1) branch.

After understanding how things work in this static site stack it feels very natural and I'm wondering, why we were using server-side processing of static sites all the years.

I can really recommend to have a look at [Hugo](https://gohugo.io) or [jekyll](https://jekyllrb.com), which as written in Ruby. It may changes the way you think about static content creation.