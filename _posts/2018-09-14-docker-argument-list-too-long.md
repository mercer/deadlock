---
layout: post
title:  "Unable to execute /usr/bin/docker: Argument list too long"
date:   2018-09-14 13:30:00
categories: linux
---

If you get this error

{% highlight bash%}
unable to execute /usr/bin/docker: Argument list too long
{% endhighlight %}

It may be that you're passing too many arguments to docker. The limitation comes from the fact that [linux commands accept a maximum size](https://stackoverflow.com/questions/11289551/argument-list-too-long-error-for-rm-cp-mv-commands).

Try limiting the command, for example:

{% highlight bash%}
docker volume ls -qf dangling=true | head -n 1000 | xargs -r sudo docker volume rm
{% endhighlight %}
