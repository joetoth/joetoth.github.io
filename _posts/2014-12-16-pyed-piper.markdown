---
layout: post
title:  "Pyed Piper, sed and awk alternative"
date:   2014-12-16 15:24:47
categories: programming
---

As much as I love looking up sed/awk commands (or writing java)  for one-off
text processing Pyed Piper seems to be a super easy alternative.
[https://code.google.com/p/pyp/][pyp]

Just converted a class with inline comments that look like:

{% highlight java %}
public Picture picture() // current picture
{% endhighlight %}

to

{% highlight java %}
 /**
  * current picture
  */
 public Picture {}
{% endhighlight %}

with the following command (and re-format with my IDE):

{% highlight bash %}
cat Seam.java | pyp "slash | '/**\n*' + p[2] + '\n*/\n' + p[0] +'{}' "
{% endhighlight %}

[pyp]: https://code.google.com/p/pyp/
