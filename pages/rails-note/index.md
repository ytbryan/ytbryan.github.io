---
title: 'Rails Note: Responsibility of each layer'
author: ytbryan
layout: page
---
These are some guidelines I follow for my own rails development.

Pick erb, coffeescript over haml and javascript

Controllers &#8211; anything that facilitates view and models.

Controller Concerns &#8211; found in controllers are modules for controllers. Place any repeatable controllers code here.

Models &#8211; anything that interact with database

Models Concerns &#8211; found in controllers are modules for controllers. Place any repeatable models code here.

View &#8211; anything that you can see on webpage. Try to use only erb and html.

Helpers &#8211; are modules for views. Try to keep anything rendering html

Assets/Javascript

Assets/Stylesheets

======

To rollback migration

<pre class="lang-rb prettyprint prettyprinted"><code>&lt;span class="pln">rake db&lt;/span>&lt;span class="pun">:&lt;/span>&lt;span class="pln">rollback STEP&lt;/span>&lt;span class="pun">=&lt;/span>&lt;span class="lit">1&lt;/span></code></pre>

Heroku

[Avoid idling][1]

&nbsp;

**common mistakes in rails **

http://www.toptal.com/ruby-on-rails/top-10-mistakes-that-rails-programmers-make

[A quick guide to installing rails on some platforms][2]

[include your active record in your ruby script][3]

&nbsp;

Use asset pipeline to arrange the javascript dependencies. First, drop your javascript into assets/javascript/<folder>. Then go to application.js to include the dependencies if you need the order to be sorted.

If your javascript depends on certain javascript to be loaded first, simply go to application.js and add //=require <relative\_path>/<name\_of\_js\_omit_.js>

commenting out erb in rails  
http://stackoverflow.com/questions/8514946/how-do-i-comment-out-erb-in-rails

 [1]: https://coderwall.com/p/u0x3nw/avoid-heroku-idling-with-new-relic-pings
 [2]: https://gorails.com/setup/ubuntu/14.10
 [3]: http://snippets.aktagon.com/snippets/257-how-to-use-activerecord-without-rails