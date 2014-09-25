---
layout: page
title: JSON Schema
profile_type: link_profile
permalink: /json-schema/
---

**PROFILE:** http://profiles.hyperfriendly.net/json-schema

The JSON Schema profile adds the following semantics to a link.

The link MUST contain a schema element conforming to the [JSON Schema spec](http://json-schema.org/)

{% highlight javascript %}
{
  "_links": {
    "create": {
      "href": "/users",
      "linkProfiles": [ "http://profiles.hyperfriendly.net/json-schema" ]
      "schema": {
        "title": "Create user",
        "type": "object",
        "properties": {
          "firstName": {
            "type": "string",
            "required": true
          },
          "lastName": {
            "type": "string",
            "required": true
          },
          "address": {
            "type": "object",
            "properties": {
              "street": {
                "type": "string"
              },
              "postalCode": {
                "type": "integer",
                "minimum": 0,
                "maximum": 9999
              }
            }
          }
        }
      }
    }
  }
}
{% endhighlight %}

JSON Schema supports referencing other schema which means that the resource does not need to contain the entire schema.

{% highlight javascript %}
{
  "_links": {
    "profile": {
      "href": "http://profiles.hyperfriendly.net/json-schema"
    },
    "create": {
      "href": "/users",
      "method": "POST",
      "schema": {
        "$ref": "http://api.test.com/schema/new-user.json"
      }
    }
  }
}
{% endhighlight %}
