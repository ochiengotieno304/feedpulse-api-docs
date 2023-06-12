---
layout: page
title: Getting Started
nav_order: 2
has_children: true
permalink: /getting-started/
---

## Create Account

Create an account through the `/account/new` endpoint

{% highlight shell %}
curl --location 'http:///api/account/new' \
--header 'Content-Type: application/json' \
--header 'Accept: application/json' \
--data-raw '{"username": "example", "email": "email@example.com"}'
{% endhighlight %}

### Parameters

- username `String` `Required`
- email `String` `Required`


### Response

The response is a json object containing user object, and token.
A refresh token is sent with the response, save it to avoid account loss on access token expiration

{% highlight shell %}
{
    "message": "account registered successfully, save refresh token to avoid account loss",
    "user": {
        "id": 9,
        "username": "example",
        "email": "email@example.com",
        "refresh_token": "secret-refresh-token"
    },
    "token": "secret-access-token"
}
{% endhighlight %}

## Confirm Email

Confirm email to activate your account
