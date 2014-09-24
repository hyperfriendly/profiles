---
layout: page
title: Collection
profile_type: resource_profile
permalink: /collection/
---

**PROFILE:** http://profiles.hyperfriendly.net/collection

A collection resource MUST contain an _items array. The collection resource MAY contain a next link and MAY contain a prev link.

{% highlight javascript %}
{
  "_links" : {
    "profile": {
      "href": "http://profiles.hyperfriendly.net/collection"
    },
    "self": {
      "href": "/users/page=2"
    },
    "next": {
      "href": "/users?page=3"
    },
    "prev": {
      "href": "/users?page=1"
    }
  },
  "_items": [
    {
      "_links": {
        "self": {
          "href": "/users/11"
        }
      },
      "name": "A user"
    },
    {
      "_links": {
        "self": {
          "href": "/users/12"
        }
      },
      "name": "Another user"
    }
  ]
}
{% endhighlight %}