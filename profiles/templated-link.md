---
layout: page
title: Templated link
profile_type: link_profile
permalink: /templated-link/
---

**PROFILE:** http://profiles.hyperfriendly.net/templated-link

A templated link href MUST contain a templated URI conforming to the [spec](http://tools.ietf.org/html/rfc6570)

{% highlight json %}
{
  "_links" : {
    "linkProfiles": [ "http://profiles.hyperfriendly.net/templated-link" ],
    "usersbyname": {
      "href": "/users{?name}"
    }
  }
}
{% endhighlight %}