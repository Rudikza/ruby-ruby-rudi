---
layout: post
title: "Gems for Africa"
date: 2013-11-29 08:49:41 +0200
comments: true
categories: 
---

So our good friends over at [Cloud Africa](https://www.cloudafrica.net/) are now hosting a mirror of rubygems. Niiice!

To use this repo in your favorite rails project just change the top line in your Gemfile from this:

{% codeblock lang:ruby [Gemfile] %}
source "https://rubygems.org"
{% endcodeblock %}

to this:

{% codeblock lang:ruby [Gemfile] %}
source "https://gems.cloudafrica.net"
{% endcodeblock %}

and prepare to be amazed.

To use this mirror for your command line gems you can do the following:

{% codeblock %}
$ gem source -r https://rubygems.org/
$ gem source -a https://gems.cloudafrica.net/
$ gem source -a https://rubygems.org/
{% endcodeblock %}

First, we remove the official rubygems site, then we add in the cloud africa repo, then add in rubygems again, just in case.
