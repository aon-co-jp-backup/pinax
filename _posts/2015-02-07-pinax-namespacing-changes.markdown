---
layout: post
title:  "Pinax Namespacing Changes"
date:   2015-02-07 20:31:04
categories: announcements
---
Until recently, Pinax apps had no consistent naming scheme. Some things were
named for function like [pinax-wiki][wiki], others didn't have Pinax in
the name like [django-user-accounts][DUA], and yet others had Greek names like
[anafero][anafero].

The history behind this stems from not being able to package namespaces when
Pinax got started. With the recent effort by Eldarion to [danate their open source][donate]
to the Pinax organziation, the Pinax team is making extra effort to clean
code up, add documentation, etc. Part of this effort caused us to rethink
the namespacing issue as well as the simple, functional names this would enable.

Some projects have already been converted over but there is still much to do.

You will start seeing some projects you are familiar with renamed and all of
them dropped under a top level `pinax.*` namespace.

The thing that enables namespace packages is this bit:

{% highlight python %}
# pinax/__init__.py
from pkgutil import extend_path
__path__ = extend_path(__path__, __name__)  # noqa
{% endhighlight %}

This will tell `setup.py` to append to this folder in your `site-packages`
instead of copying over it so as you install multiple Pinax packages you'll have
a folder in `site-package/pinax/` that gets additional sub-packages added to it.

We feel that will provide as stronger sense of an ecosystem and allow for great
apps to be more easily discovered.

As we rename apps and/or convert them to a namespaced version of their prior
selves, we'll announce it here on this blog.

[wiki]:    https://github.com/pinax/pinax-wiki/
[DUA]:     https://github.com/pinax/django-user-accounts/
[anafero]: https://github.com/eldarion/anafero
[donate]:  http://eldarion.com/blog/2014/09/23/donating-pinax/

