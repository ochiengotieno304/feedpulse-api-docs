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
curl --location --request POST 'http://api.feedpulse.com/account/new' \
--header 'Accept: application/json' \
--header 'Content-Type: application/json' \
--data '{"username": "testuser", "email": "test@mail.com"}'
{% endhighlight %}

### Parameters

- username `String` `Required`
- email `String` `Required`


### Response

The response is a json object containing user object, and an api key. Store the api key securely.

{% highlight json %}
{
    "message":"account registered successfully",
    "user_details":{
        "username":"testuser",
        "email":"test@mail.com",
        "api_key":"secret-api-key"}
}
{% endhighlight %}

## Confirm Email

Your'll receive a confirmation email to activate your account
