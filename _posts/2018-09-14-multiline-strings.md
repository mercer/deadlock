---
layout: post
title:  "Multi-line strings"
date:   2018-09-14 12:30:00
categories: java
---

Multi-line strings in source code are quite useful. You can use them as an embedded template engine, for example to construct the body of a REST call.

Groovy is one language that has [multi-line strings](http://groovy-lang.org/syntax.html).

{% highlight groovy %}
def aMultilineString = '''line one
line two
line three'''
{% endhighlight %}

In [python](https://docs.python.org/3/tutorial/introduction.html#strings) you have

{% highlight python %}
s = """ this is a very
        long string if I had the
        energy to type more and more ..."""
{% endhighlight %}

For javascript you still need to escape backslashes

{% highlight javascript %}
var multiStr = "This is the first line \
    This is the second line \
    This is more...";
{% endhighlight %}

Perl has them too

{% highlight perl%}
my $message = <<'END_MESSAGE';
Dear $name,

this is a message I plan to send to you.

regards
  the Perl Maven
END_MESSAGE
{% endhighlight %}

And of course, [Kotlin](https://kotlinlang.org/docs/reference/basic-types.html)

{% highlight kotlin%}
val text = """
    for (c in "foo")
        print(c)
"""
{% endhighlight %}

Java might get the multiline with [JEP 326](http://openjdk.java.net/jeps/326). It will look like this

{% highlight java%}
String html = `<html>
                   <body>
                       <p>Hello World.</p>
                   </body>
               </html>
              `;
{% endhighlight %}
