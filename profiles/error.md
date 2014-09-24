---
layout: page
title: Error
profile_type: resource_profile
permalink: /error/
---

**PROFILE:** http://profiles.hyperfriendly.net/error

An error resource MUST contain an _errors collection. A error item MUST have a title and a message.

{% highlight json %}
{
  "_links" : {
    "profile": "http://profiles.hyperfriendly.net/error"
  },
  "_errors": [
    {
      "title": "Some error",
      "message": "Some error has occurred"
    }
  ]
}
{% endhighlight %}