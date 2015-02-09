---
layout: post
title: "django-haystack 1.2.2 Release Notes"
date: 2011-05-20 00:50:33
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-haystack/django-haystack-1.2.2.tar.gz>

This release includes the following:

* Require Whoosh 1.8.3+. It's for your own good.
* Added multiprocessing support to ``update_index``! Thanks to CMGdigital / for funding development of this feature.
* Fixed a bug where ``set`` couldn't be used with ``__in``. Thanks to Kronuz for the report!
* Added a ``DecimalField``.
* Fixed a bug where a different style of import could confuse the collection of indexes. Thanks to groovecoder for the report.
