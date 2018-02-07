---
layout: post
title: Build a blog with Jekyll on Github Pages
tags: [Jekyll]
---

I'm kind of getting bored memorizing what I learned on my notebooks. And by chance I found some brilliant blogs built on Github Pages. Maybe now is the right time for me to learn building my own blog as my public notebook.

## 1. Fork a online theme

There are so many awesome themes available so we don't need to build from nothing.[jekyllthemes](http://jekyllthemes.org/) is what I use to find themes.

After fork a theme project on Github, you need to change its name to **\<yourname\>.github.io**. Okay! Now Github will automatically detect this name and start your server running on \<yourname\>.github.io.

## 2. Clone this project

Let's clone the project to your own computer. We will edit blog files offline. Once we finished a new blog we can just push this project to Github and our server will be regenerated.

Seem that its okay to start write your first post.

## 3. Write a post

To create a new post, all you need to do is create a file in the \_posts directory. How you name files in this folder is important. Jekyll requires blog post files to be named according to the following format:
```
YEAR-MONTH-DAY-title.MARKUP
```
Where YEAR is a four-digit number, MONTH and DAY are both two-digit numbers, and MARKUP is the file extension representing the format used in the file.

Inside this file, we need to write a header for Jekyll to recognize the attribute of this post. A standard blog style post, including a Title, Layout, Publishing Date, and Categories might look like this:
```Markdown
---
layout: post
title:  "Welcome to Jekyll!"
date:   2015-11-17 16:16:01 -0600
categories: jekyll update
---

You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. You can rebuild the site in many different ways, but the most common way is to run `bundle exec jekyll serve`, which launches a web server and auto-regenerates your site when a file is updated.
```

To add new posts, simply add a file in the `_posts` directory that follows the convention `YYYY-MM-DD-name-of-post.ext` and includes the necessary front matter. Take a look at the source for this post to get an idea about how it works.
Everything in between the first and second --- are part of the YAML Front Matter, and everything after the second --- will be rendered with Markdown and show up as “Content”.

However, you will find it troublesome to check the changes after edit. You have to `commit` changes `push` to Github and wait for its regeneration. Is there any way I can write my blog offline and check it before pushing to the server?

Yes there is. That Why we need to install Jekyll.

## 4. Install Jekyll

Install ruby first. And then you can use `gem` to install Jekyll:
```shell
gem install jekyll
cd path/to/blog
bundle install
bundle exec jekyll serve
```
That's all! Now a server is running on your computer. It will automatically detect changes and regenerate new web pages.

## 5.Further customization

To deeply customize your blog, you need some konwledge of [Jekyll](https://jekyllrb.com/) and, of course, HTML CSS JS. That too much for this startup tutorial.

That's it, hope you enjoy!
