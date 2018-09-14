---
layout: post
title:  "Use HttpsURLConnection for a secure connection"
date:   2018-09-14 13:00:00
categories: java
---

You want to connect to a https server, let's say https://api.github.com/. What do you use, HttpURLConnection or HttpsURLConnection?

HttpURLConnection is an URLConnection with support for http specific features, such as HTTP_CLIENT_TIMEOUT.

HttpsURLConnection extends HttpURLConnection and adds specific https features, such as SSL.

What I understand from here is that, if you want your connection to be corretly encrypted, and you do, then use HttpsURLConnection when you create a connection to a https server instead of using HttpURLConnection.
