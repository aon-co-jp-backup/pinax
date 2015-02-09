---
layout: post
title:  "Pinax Donations and Namespacing"
date:   2015-02-07 20:31:04
categories: announcements
---
Pinax was born as a single repository with bundled projects, apps, and themes.

In 2012, however, we began the process of unbundling it by pulling out the
accounts app and giving birth to [django-user-acounts][DUA] to signal that while
a framework, individual apps can easily stand on their own. Very quickly, the
main [Pinax repo][pinax-repo] came to be just a README with all the individual
apps, starter templates, and themes living in their own repos and packages under
the [Pinax org][pinax-org].

Beginning in late 2014, [Eldarion][eldarion.com] began donating a host their
open source Django apps to the [Pinax org][pinax-org]. In the process, decisions
were made to rename their oft Greek-inspired naming schemes to follow a more
conventional and functional naming.

We decided during this process to make the names as functional as possible. One
side affect of this is using names that are most certainly naming collisions for
top level packages, so we decided to namespace them under `pinax.*`.

We want to be clear, though, that with very few exceptions, all these apps
stand on their own and there are not requirements other than you are using
Django. Where there are exceptions, it is where it makes sense for an app to
leverage functionality from another ecosystem app.

For those who are interested in just how we create namespaced packages, we
wanted to share this tidbit that we spent some time figuring out:

{% highlight python %}
# pinax/__init__.py
from pkgutil import extend_path
__path__ = extend_path(__path__, __name__)  # noqa
{% endhighlight %}

This will tell `setup.py` to append to this folder in your `site-packages`
instead of copying over it so as you install multiple Pinax packages you'll have
a folder in `site-package/pinax/` that gets additional sub-packages added to it.

So, to be clear, Pinax is an ecosystem of apps, starter projects, and themes. We
have written most of them ourselves and they live under the [Pinax org][pinax-org],
but the ecosystem can and has extended beyond this org as evidenced by all the
apps under [Eldarion org][eldarion-org] that are being donated to Pinax.


[pinax-org]:    https://github.com/pinax/
[DUA]:     https://github.com/pinax/django-user-accounts/
[eldarion-org]: https://github.com/eldarion/
[pinax-repo]:  https://github.com/pinax/pinax/
