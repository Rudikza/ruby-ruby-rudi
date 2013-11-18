---
layout: post
title: "Guard::RSpec DEPRECATION WARNING: The :cli option is deprecated"
date: 2013-11-18 20:06:45 +0200
comments: true
categories: [Rails 4, Guard, Spork, RSpec]
---

So I recently created a new rails 4 app and after doing my usual setup and starting up guard I started getting this deprecation warning.

{% codeblock %}
 Guard::RSpec DEPRECATION WARNING: The :cli option is deprecated
{% endcodeblock %}

Hmm, so it looks like RSpec is going to deprecate the :cli option and now wants us to use :cmd. After some digging I found that replacing this line:

{% codeblock lang:ruby [Guardfile] %}
guard 'rspec', :cli=>'--drb', all_on_start: false, all_after_pass: false do
{% endcodeblock %}

with this one:
{% codeblock lang:ruby [Guardfile] %}
  guard 'rspec', :cmd=>'rpec --drb', all_on_start: false, all_after_pass: false do
{% endcodeblock %}

