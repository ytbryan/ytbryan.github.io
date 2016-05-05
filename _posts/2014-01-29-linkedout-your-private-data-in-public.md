---
title: 'Linkedout &#8211; your private data in public'
author: ytbryan
layout: post
permalink: /linkedout-your-private-data-in-public/
categories: work startup uncategorized
tags:
hefo_before:
  - 0
hefo_after:
  - 0
dsq_thread_id:
  - 2191454416
---
**TL;DR**: LinkedIn email subscription uses no [auth token][1]. This means that anyone can manipulate your email subscription without your approval.

To find out how I discover it and other possible implications, read on!

<a style="font-size: 14px; line-height: 1.5em;" href="http://ytbryan.com/wp-content/uploads/2014/01/c5fdf0f7704a7934c10febdacd77ca98.jpg"><img class="alignnone size-full wp-image-1191" alt="c5fdf0f7704a7934c10febdacd77ca98" src="http://ytbryan.com/wp-content/uploads/2014/01/c5fdf0f7704a7934c10febdacd77ca98.jpg" width="500" height="489" /></a><span style="font-size: 14px; line-height: 1.5em;"> </span>

I received a linkedIn request from a fellow entrepreneur to connect. Since I&#8217;m mostly inactive on linkedIn, I opened the email and clicked on the unsubscribe link (see below)

[<img class="alignnone size-full wp-image-1245" alt="wah" src="http://ytbryan.com/wp-content/uploads/2014/01/wah.png" width="772" height="470" />][2]

The unsubscribe link brings me to the unsubscribe page without authentication. I proceed to click &#8220;Save&#8221; (See below)

<img class="alignnone size-full wp-image-1237" style="font-size: 14px; line-height: 1.5em;" alt="2" src="http://ytbryan.com/wp-content/uploads/2014/01/2.png" width="1234" height="381" />

Everything went smoothly and my email settings got updated! (See below)

<img class="alignnone size-full wp-image-1238" style="font-size: 14px; line-height: 1.5em;" alt="3" src="http://ytbryan.com/wp-content/uploads/2014/01/3.png" width="1063" height="125" />

But wait! Why are these settings not protected by an authentication token or service?

### How anyone can edit your linkedIn email setting:

**1. Edit the email subscription url with a different email.** (Click [here][3] for the email subscription url.)

http://www.linkedin.com/settings/

email-unsubscribe?

id=20008&

mid=224988018&

aid=72gtpjsvfahq7sh&

email=xxx%40gmail%2Ecom& <span style="color: #ff0000;"><strong>(Edit this part)</strong></span>

eid=-nmd1bo-hqq84r03-4c

**2. Paste the edited url into the browser and you will see a new  email setting page. Without authentication. **

By varying the email, anyone can change the email subscription setting without the owner&#8217;s approval.

This begs the question:

1. Why is the email subscription not protected with a security token or sit behind an authentication service? Is the email subscription not part of Linkedin privacy concern?

2. Which other api of Linkedin are not protected?

3. How will this affect paid users since (I assume) they rely on email for businesses?

 [1]: http://en.wikipedia.org/wiki/Security_token
 [2]: http://ytbryan.com/wp-content/uploads/2014/01/wah.png
 [3]: http://www.linkedin.com/settings/email-unsubscribe?id=20008&mid=224988018&aid=72gtpjsvfahq7sh&email=xxx%40gmail%2Ecom&eid=-nmd1bo-hqq84r03-4c
