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
To set up my personal Github pages, I decided to use a static site stack.

The idea is, instead of using a huge and slow CMS like WordPress or Drupal, to simply upload only static HTML and asset files. Neither the dynamic, server side rendering of the pages, nor a database is required.

You simply put your content as Markdown files into a tree structure, which represents your site structure and the static site generator turns it into a bunch of HTML files which you can upload to your server.

For the generation of the site I'm using [HUGO](https://gohugo.io), a site generator which is written in Go and is available for Linux, Windows and MacOS.

Hugo allows you to setup a complete website just with some commands, a little configuration file and your content files written in Markdown. Although it has an extensive documentation, it is sometimes hard to find the information you are looking for due to the huge amount of things you can use Hugo for.

The benefit of using a site generator is, that you can work with your familar Git workflow. Whether your trying out a new feature or whether you want to revert to an older state, Git allows you to do so!

Another great feature of using git is that it allows you to write your content offline. You can simply push your changes to the deployment environment when you're connected to the internet again.

[forestry.io](https://forestry.io) sits on top of such a site generator like Hugo and provides a graphical user interface like a traditional CMS to you or even your team. Although you don't need a GUI to run Hugo, it is a very handy way to edit your content for example from your mobile phone (like I'm doing now) as it features a content editor with WYSIWYG preview, a simplified process of publishing your changes and much more. In contrast to Hugo itself, which runs on your local development machine, forestry.io is a hosted service which is free for personal use.

But why [GitHub](https://github.com)? One reason is that I'm using GitHub as a remote repository for Hugos source files (the markdown and the configuration of this site). But with the help of forestry.io it is really easy to deploy the generated files directly to a branch which is connected to GitHub pages.

This sites source is stored for example in the [src](https://github.com/dubst3pp4/dubst3pp4.github.io/tree/src?files=1) branch of my repository, while the site is generated into the [master](https://github.com/dubst3pp4/dubst3pp4.github.io/tree/master?files=1) branch.

As easy as that!