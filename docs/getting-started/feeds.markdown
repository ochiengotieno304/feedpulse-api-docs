---
layout: page
title: Get Feeds
parent: Getting Started
nav_order: 1
permalink: /getting-started/feeds/
---

# Your First Request

The FeedPulse API uses bearer token for request authentication

``` shell
curl --location 'http://localhost:2300/api/feeds?country=ke' \
--header 'Accept: application/json' \
--header 'Authorization: Bearer your-secret-token'
```

``` ruby
puts 'hello'
```
