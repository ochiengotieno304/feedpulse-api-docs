---
layout: page
title: Account
parent: Getting Started
nav_order: 1
permalink: /getting-started/account/
---

# Refresh Token

To refresh access token send 

{% highlight shell %}
curl --location 'http://localhost:2300/api/feeds?country=ke' \
--header 'Accept: application/json' \
--header 'Authorization: Bearer your-secret-token'
{% endhighlight %}

``` ruby
puts 'hello'
```
