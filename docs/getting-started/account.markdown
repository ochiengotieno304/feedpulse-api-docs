---
layout: page
title: Account
parent: Getting Started
nav_order: 1
permalink: /getting-started/account/
---

# Revoke API Key

> **Warning**
> **Deprecated**, use [RapidAPI](https://rapidapi.com/ochiengotieno304/api/feedpulse2) to access FeedPulse

To revoke your api key make this request

{% highlight shell %}
curl --location POST 'http://api.feedpulse.test/account/revoke-key' \
--header 'Accept: application/json' \
--header 'Authorization: secret-api-key' \
--data '{"username": "your-user-name"}'
{% endhighlight %}
