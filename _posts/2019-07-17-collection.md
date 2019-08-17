---
layout: post
title: "Example Twitter Collection Timeline"
date: 2019-07-17 13:58:05 -0700
categories: twitter examples
twitter-timeline:
  name: TwitterDev
  text: National Park Tweets
  type: collection
  collection: 539487832448843776
  chrome: nofooter noscrollbar noborders transparent
  tweet_limit: 3
  width: 800
  inject_js: true
---


**Example FrontMatter**


```MarkDown
---
twitter-timeline:
  name: TwitterDev
  text: National Park Tweets
  type: collection
  collection: 539487832448843776
  chrome: nofooter noscrollbar noborders transparent
  tweet_limit: 3
  width: 800
  inject_js: true
---
```


**Example HTML**


```HTML
<a class="twitter-timeline"
   href="https://twitter.com/TwitterDev/timelines/539487832448843776"
   data-width="800"
   data-height="600"
   data-chrome="nofooter noscrollbar noborders transparent"
   data-tweet-limit="3">National Park Tweets</a>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
```


**Example output**


> Note, the following is **not** associated with this site and is referred to only to remain consistent with official Twitter API documentation
