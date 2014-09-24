---
layout: page
title: Feed
profile_type: resource_profile
permalink: /feed/
---

**PROFILE:** http://profiles.hyperfriendly.net/feed

A feed is a special [collection](https://github.com/hyperfriendly/spec/wiki/Resource-profile:-Collection) where the payload is an event wrapped in a special envelope. It contains a history of events and can be chained using next and prev links. A feed MUST conform to the collection profile.

The envelope MUST contain a messageType, sequenceNumber and a body object. It MAY contain a headers object with metadata.

{% highlight javascript %}
{
  "_links" : {
    "profile": "http://profiles.hyperfriendly.net/feed"
  },
  "_items": [
  {
    "messageType": "SomethingHappened",
    "sequenceNumber": 1,
    "body": {
      "foo": 1,
      "bar": "something"
    },
    "headers": {
      "meta": "data"
    }
  }
  ]
}
{% endhighlight %}