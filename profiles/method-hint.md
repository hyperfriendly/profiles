---
layout: page
title: Method hint
profile_type: link_profile
permalink: /method-hint/
---

**PROFILE:** http://profiles.hyperfriendly.net/method-hint

The method hint profile adds semantics to a link in the following way.

The link MUST contain a *method* element that describes which HTTP method should be used to interact with the resource.

{% highlight javascript %}
{
  "_links": {
    "profile": {
      "href": "http://profiles.hyperfriendly.net/method-hint"
    },
    "add_user": {
      "href": "/users",
      "method": "POST"
    }
  }
}
{% endhighlight %}