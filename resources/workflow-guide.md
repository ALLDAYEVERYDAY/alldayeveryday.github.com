---
layout: page
title: "The Workflow Guide"
group: resources
---

## Project Set Up

1. Develop brief; client sign-off.
2. SOW developed; clients sign-off.
3. On sign-off, invoice schedule sent to Tim.
4. On sign-off, resources booked.
5. Dev setup:
    - Dev, Staging, and Production servers
    - DNS information
    - SSL certificate setup
    - Analytics
6. Client assets delivered (brand guidelines, content, etc).

## Discovery and Creative Development

1. Project Kickoff
    - Assign team
    - Brief everyone
    - Assign KPIs

## Init to Design Checklist

1. Content, get some actual samples if possible
2. Client control over content? what is to be editable? not? 
3. BETA details. who will be testing it? 

## Design

1. Design kickoff
   Design as usual, sign-off at each client stage needs to be by:
   - Art Director
   - Design Technologist
   - Developers on the project
   - Digital Director

## Design to Dev Checklist

1. Image Assets
    - any graphical content that can't be rendered using css. Should be cropped to the smallest possible size.  If it's a set of icons or similar, use [css sprites](http://www.alistapart.com/articles/sprites)
    - if deploying on mobile devices, ensure image content is rendered at double size to accomodate retina display (NOTE: include iphone dimensions??)
1. Design Assets. PDF/PNGs of designs as well as production files
2. Color palette
    - Swatch of all colors in design. Include rgb/hex
    - link colors?
3. Custom fonts
    - acceptable formats: otf, ttf
    - include size, line heights, kerning, etc. for different treatments throughout the site (general copy, h1, h2)
4. On/off/hover states of buttons, labels.
5. Content dimensions - overlay on orig designs?
    - for browser based content, include width/height (pixels) of outermost visible content for scale
    - for mobile deploys, include all dimensions of content that does not conform to each platforms mobile standards.
        - [webkit/ios](http://www.idev101.com/code/User_Interface/sizes.html)
6. All content packaged in zip format
7. Identify problem areas in user/client generated content. (eg. could a dynamic title be too large for the designed space?)
8. Are all the various html elements covered by the design? For example, if designing a block, what's a blockquote going to look like? What's a general form supposed to look like?

## Development

1. Dev kickoff (after designs get to a reasonable point)
    - Both developers + producer + digital director need to be present
    - The producer should be aware of things that are either ambiguous or out of the defined scope, and be prepared to discuss findings with the client ASAP after the kickoff.
2. Project architecture & planning
    - Define data model
    - Revise dev schedule (we should set expectations with the clients that dev dates might shift based on designs)
3. Hosting requirements & estimate developed
    Developers can do this in conjunction with the producer. Fees can include:
    - Heroku capacity
    - Add-ons (New Relic, Exceptional, etc.)
    - 3rd party services (Pusher, Redis, etc.)
    - S3 asset storage and bandwidth estimate (usually trivial, but we should account for it and our agreement language should be flexible enough to say we can bill more if S3 fees exceed our estimate)
    - SSL renewal

    The hosting estimate needs to be finalized and signed off on prior to launch. We should establish a baseline fee of ??? billed at 6-month intervals.
4. Development proceeds. Beta links need to be ready at least one day ahead of client delivery and reviewed/signed off on by:
    - Art Director
    - Design Technologist
    - Digital Director

## Dev to Production Checklist

1. Timezone. 
    ensure TZ env variable is set on all servers. in term: 
    Linux: TZ=[Area]/[Location]; export TZ;
    Heroku: heroku config:add TZ=[Area]/[Location]
2. New Relic
    Must be installed on all production servers. (Q paid:standard)
    [install instructions](http://devcenter.heroku.com/articles/newrelic)
3. Supported Platforms
    - IE 8+
    - Chrome
    - Mozilla Firefox 4+
    - Safari 4+
    - iOS5
    - Android: Ice Cream Sandwich
4. Ensure proper scale
   Worker dynos = expensive. Dev/Staging sites should not have running workers after launch. Dev/staging sites should also not have more than one web dyno.
5. Use the Procfile
   Ensure production apps are not launched with Webrick server. Use Thin or Mongrel
6. Memcache when possible
   [see Dalli gem](https://github.com/mperham/dalli)
7. Custom 401,404,500 pages
8. SSL Certificates for login pages (godaddy, MT, verisign?)
    Nike has their own route! Needs to be internal

## Content Integration

Needs to be planned/scheduled in advance. In an ideal world we can offload this responsibility to the clients

## Documentation & Training

We should do this!

## QA

1. Develop QA estimate (either using internal resources or with a 3rd party vendor). Ideally this is the same amount of time allotted in the SOW.
2. Estimate needs to be approved by the Director of Operations if it exceeds ??% or $?? on top of the initial estimate.
3. Schedule QA time.
4. Proceed with QA.
5. If major issues are uncovered, the producer may need to inform the client of delays in schedule.

## Launch

A full day should be allocated for launch for both the producer and one of the project developers. 

The process should loosely be:

- Backup any existing website/assets
- Add custom domains to the production Heroku app
- Follow the launch checklist for the appropriate platform
- Final QA on .production.alldayeveryday.com site
- Ask for final client sign-off
- On sign-off, put DNS records live
- Follow-post-launch checklist
- Remove .production.alldayeveryday.com custom domain 

Developers and the producer should be on-call for 48 hours post-launch to address any lingering issues.

## Post Production/Launch Discussion

1. Successes, failures, improvements
2. Assemble reusable code.

## Optimize

Are we retained to optimize the site post-launch?

Things to optimize around include:

- Performance tuning
- A/B testing and landing page/funnel optimization
- Social sharing & performance
- SEO
- New feature recommendations

## General Discussion/Suggestions

1. Deployment services? When to use what?

    We should probably use Heroku for everything, and only 1 other service for things that demand a more traditional server environment
    - Heroku
    - Amazon EC2
    - Joyent
    - Media Temple Grid Service (Assets status?)
2. Tech Stack
    - Ruby on Rails (3.2)
    - Sinatra
    - Pure Rack
    - Ruby >= 1.9.2
    - Php >= 5.3?
    - Postgres >= 8.3
    - Sencha Touch 1,2
    - Backbone JS
    - CoffeeScript
    - jQuery 1.7.1
3. Development Environment
    - Postgres
    - POW Server
    - Webrick
    - Thin
    - Tumblrs: strategy for development
    - Organization: Basecamp, kickoff, lighthouse?
3. how are assets handed off from PMs to Designers to DEVs? Can't be through email anymore
4. Admin Options
    - Typus
    - Rails Admin
    - Active Admin
5. Pair programming
    Every project has at least a Primary and Secondary dev?
6. Security, password protection, an actual policy for what happens when somebody leaves the company