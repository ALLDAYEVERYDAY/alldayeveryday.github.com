---
layout: page
title: "The Platform Guide"
group: resources
---

Every web platform has its strengths and limits. Limits, mostly. This document will guide you through the limits of our most common platforms.

- Ruby on Rails
- Tumblr
- Mobile Web (iOS & Android)

## Ruby On Rails

Everything is possible. As long as you follow the guidlines in the [Designer's Guide] and clear your design with the project's developer before you ship it, you're kicking ass.


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

- Photos can't be wider than 500 pixels, except in Photo Posts.
- Photo, Video, Quote, and Audio posts do not have titles.
- Text, Link, and Chat posts *do* have titles.
- Tumblr's search function doesn't work. Do not put a search bar in a Tumblr project.
- Tumblr's "Archive" cannot be customized, except at great expense. Do not design a custom archive unless this project's budget is insane.

## Mobile Web

If this project will support both phones and tablets, design for phones first. It's easier to add features on larger screens than to remove them on smaller ones.


### Network Speed

Remember that **most people will be using your app over an irritatingly slow cellular data connection**. 

Avoid images, nonstandard fonts, videos, and background textures unless they're absolutely essential. These all take a long time to download.

Use gradients, shadows, and solid colors, because even complicated shadows and gradients can be rendered on a phone without downloading any media.

### Locked elements

You can design a header that locks to the top, but make sure your design doesn't break when the header doesn't lock. Not all phones support locked elements.

Be extra careful when designing elements that lock to the bottom, because these are especially likely to break when they don't lock. (Even if it doesn't look broken, a navigation menu that the user must scroll down to see is useless.)

### Animations

Animations are great. Go wild.
