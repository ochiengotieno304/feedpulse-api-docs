---
layout: page
title: Get Feeds
parent: Getting Started
nav_order: 1
permalink: /getting-started/feeds/
---

# Your First Request

The FeedPulse API uses Api Key auth for request authentication added with the `Authorization` key within the request header

{% highlight shell %}
curl --location --request GET 'http://api.feedpulse.test/api/feeds' \
--header 'Accept: application/json' \
--header 'Content-Type: application/json' \
--header 'Authorization: secret-api-key' \
--data '{"username": "testuser", "country": "ke", "page": "1", "per_page": "10"}'
{% endhighlight %}

## Request Parameters

- **username** `String` `Required`: Your FeedPulse account username
- **country** `String` `Optional`: Country you want to fetch trending news, `default KE`
- **page** `String` `Optional`: For pagination, returns the N<sup>th</sup> page of feeds
- **per_page** `String` `Optional`: Feed per page, `default 10`


## API Response

Response body is an array of json feeds object

{% highlight json %}
[
  {
    "title": "Verona beat Spezia to retain Serie A status in relegation playoff",
    "snippet": "Hellas Verona secured another season in Serie A on Sunday after defeating Spezia 3-1 in their relegation playoff, with Cyril Ngonge&#39;s two goals sending&nbsp;...",
    "url": "https://www.reuters.com/sports/soccer/verona-beat-spezia-retain-serie-status-relegation-playoff-2023-06-11/",
    "source": "Reuters",
    "code": "KE",
    "date": "2023-06-12"
  }
]
{% endhighlight %}

### Parameters

- **title**: News item title
- **snippet**: Short snippet of the news item
- **url**: News item source url
- **title**: News item title
- **code**: Country code in which the news item is trending
- **date**: Date the news item was trending
