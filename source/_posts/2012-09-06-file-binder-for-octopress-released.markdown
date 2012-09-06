---
layout: post
title: "File Binder for Octopress Released"
date: 2012-09-06 18:17
comments: true
categories: Octopress plugin
---

[File Binder for Octopress](https://github.com/aycabta/octopress-file-binder)

It is difficult to attach some images or other files on a entry.
This plugin supports it very easy.

Usage
-----

Install to plugins directory.

If you wrote a entry in "source/_posts/YYYY-DD-MM-title-of-a-entiry.markdown",
you can attach the files that are given the name of "source/_posts/YYYY-DD-MM-title-of-a-entiry_filename-of-image.png" for example.
The attached file puts out into the same directory of the entry by the name of "filename-of-image.png",
in this case it is "public/blog/YYYY/DD/MM/title-of-a-entry/filename-of-image.png".
You can refer the files from the entry by img or others tags.

Replace "./" that is head of src in a img tag with config['url'] + "/blog/YYYY/DD/MM/title-of-a-entry/".
config['url'] is written in _config.yml with "url: ".
So src is published absolute path without problems
if you write {{ "{% img ./filename-of-image.png " }}%}.

Support customized permalink in _config.yml that is different from "/blog/:year/:month/:day/:title/".

Sample
------

[Previois entry in this blog](http://aycabta.github.com/blog/2012/09/05/receive-voip-settings-for-wakwak-phone/)

