---
layout: page
title: "The Platform Guide"
group: resources
---

Every web platform has its strengths and limits. Limits, mostly. This document will guide you through the limits of our most common platforms.

- [Ruby on Rails](#ruby_on_rails)
- [Tumblr](#tumblr)
- [Mobile Web](#mobile_web)

## Ruby On Rails

Everything is possible. As long as you follow the [Guide to Web Development](/resources/design-guide.html), you're kicking ass.


## Tumblr

Start with a single column of Posts. Posts come in seven types:

- Text
- Photo
- Quote
- Link
- Chat
- Audio
- Video

You must design one post of each type. But before you do, **sign into tumblr and create a post of each type in a dummy account**. This is the best way to get acquainted with Tumblr's quirks. There are many. For reference, here are a few:

- Photos cannot be wider than 500 pixels, except in Photo Posts.
- Photo, Video, Quote, and Audio posts do not have titles.
- Text, Link, and Chat posts *do* have titles.
- Tumblr's search function does not work. Do not put a search bar in a Tumblr project.
- Tumblr's "Archive" cannot be customized, except at great expense. Do not design a custom archive unless this project's budget is insane.
- Remember that some of the content on this blog will be 'reblogged' (meaning 'imported' or 'stolen') from other blogs. Reblogged content looks different. Reblog a post in your test tumblr, and design away.


## Mobile Web

If this project will support both phones and tablets, design for phones first. It is easier to add features on larger screens than to remove them on smaller ones.

### Network Speed
Remember that most people will be using your app over an irritatingly slow cellular data connection.

Avoid images, nonstandard fonts, videos, and background textures unless you absolutely need them. They all take a long time to download.

Use gradients, shadows, and solid colors, because even complicated shadows and gradients can be rendered on a phone without downloading any media.

### Locked elements
You can design a header that locks to the top, but make sure your design does not break when the header does not lock. Not all phones support locked elements.

Be extra careful when designing elements that lock to the bottom, because these are especially likely to break when they on phones that . (Even if it doesn't look broken, a navigation menu that the user must scroll down to see is useless.)

### Animations
Animations are great. Go wild.


