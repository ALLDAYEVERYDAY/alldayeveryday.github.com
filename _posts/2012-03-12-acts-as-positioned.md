---
layout: post
title: "Acts As Positioned"
category: 
tags: []
---
{% include JB/setup %}

We're pleased to announce [ActsAsPositioned](https://github.com/ALLDAYEVERYDAY/acts_as_positioned), our first open-source gem. It's available right now on [GitHub](https://github.com/ALLDAYEVERYDAY/acts_as_positioned).

We often use [RailsAdmin](https://github.com/sferik/rails_admin) or [Typus](https://github.com/fesplugas/typus) as the CMS for our projects, and though they're mostly great, they suck at organizing records by position. Slides in slideshows and songs in playlists take forever to re-order, and even if you're careful their positions usually get messed up.

It should be impossible for your CMS to let you set positions like this:

<pre>
2. Come Together
3. Something
3. Maxwell's Silver Hammer
3. Oh! Darling
16. Octopus's Garden
</pre>

But spend some time organizing a playlist in Typus, and it's likely to turn out that way or worse.

We like slideshows and playlists. They should be easy to organize, and you shouldn't have to be careful.

When you call <code>acts_as_positioned</code> on an ActiveRecord model, you can save records in whatever position you want, and your app  will adjust the rest of the list intelligently. Your lists will stay in sequence, and you won't have to think about this problem anymore.

***

### How-To

First, add it to your gemfile:

<pre>
gem 'acts_as_positioned', :git => 'git://github.com/ALLDAYEVERYDAY/acts_as_positioned.git'
</pre>

Second, run <code>bundle install</code>.

Last, use it in a model:

<pre>
class Song &lt; ActiveRecord::Base
  acts_as_positioned 
end
</pre>

***

Enjoy! You'll find the source and more documentation [on GitGub](https://github.com/ALLDAYEVERYDAY/acts_as_positioned).

