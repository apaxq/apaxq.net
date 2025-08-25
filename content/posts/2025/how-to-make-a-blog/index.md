+++
title = "How to Make a Blog"
date = "2025-09-01"
draft = true

[taxonomies]
tags=["Blog"]

[extra]
repo_view = true
comment = true
read_time = true
+++
![A flag that says "We do this not because it is easy, but because we thought it would be easy"]()

Well, I finally did it. After telling myself for ten years that I would get around to making a blog, I finally did it. 

I'm not much of a writer, but I'm trying to make it a habit. I've been told that writing/journaling is therapeutic and can be a good way to learn. 

Also, it's a good way to share my thoughts and knowledge with others. For years, I've wanted to have a platform where I can publish my thoughts and ideas and have a place to write and document the things I am working on and my learnings. 

My requirements for my blog were:
- Had to be fast (no bloated libraries or twenty thousand JavaScript files, should be able to run on most web browsers).
- Had to be easy to make (no complicated setup, just open up `vim` and publish).
- Had to be easy to read (plain text, no fancy formatting).
- Had to be secure (No database, no PHP).

## Choose your own adventure

### Option 1: Good old LAMP stack
For the uninitiated, LAMP stands for Linux, Apache, MySQL, PHP. It's a stack of open source software that is used to build websites. It was very popular in the early 2000s thanks to PHP software such as WordPress. Today if you were to take that route, you would probably use OpenBSD, Nginx, PostgreSQL, and PHP. 

While this can be a good option for some users, there are a few issues with this method of blogging. For starters, it requires the setup of a dedicated server (like an EC2 or Virtual Machine). You will also need to set up a database and configure said database with your webserver, configure PHP to work with your web server, and make sure your configs are secure. As you can imagine, giving PHP access to your database can be a security risk if you're not careful, and I really didn't want to deal with that. 

For the record, `apaxq.net` is hosted on Nginx on a OpenBSD VPS (Virtual Private Server). The reason I opted for a VPS is that I plan on using `apaxq.net` to run additional services, such as a personal email server, a file server, VPN server, and might even run a few other websites for friends and business partners (using Nginx reverse proxy features). If it weren't for the fact that I have big plans for `apaxq.net`, I probably would have opted to run a static website on AWS. 

Additionally, I don't want to deal with the hassle of using a web UI to publish content and manage my website. Not only is it cumbersome, but it also opens you up to security vulnerabilities.

### Option 2: Blog platform
So if you're like me, and you don't want to deal with the hassle of setting up a LAMP stack and deal with the security burdens, you can use a blog platform. Blog platforms allow you to manage and post your content without having to worry about the underlying infrastructure. 

Some popular blog platforms include [WordPress](https://wordpress.com/) (not to be confused with [WordPress](https://wordpress.org/)), [Blogger](https://www.blogger.com/), [Tumblr](https://www.tumblr.com/), [Medium](https://medium.com/), [X](https://x.com), ([yeah they have one too](https://help.x.com/en/using-x/articles)), and more recently [Substack](https://substack.com/about)

### Option 3: Static site generator
After a while, I kinda decided that maybe my dream of simple blogging wouldn't be possible. But then one day while researching an issue I was having with React, I ran across [Dan Abramov](https://danabra.mov) personal blog [overreacted](https://overreacted.io)

#### Option 3.1: Gatsby

#### Option 3.2: Jekyll

#### Option 3.4 Zola
So far everything looked very complicated and not very well organized. But then one day while trying to resolve an issue in OpenBSD, I ran across [Wesley Moore's Blog](https://www.wezm.net/v2/) (by the way, [thanks for solving my problem](https://www.wezm.net/v2/posts/2023/openbsd-db-atapi-start-not-ready/).