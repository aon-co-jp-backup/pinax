---
layout: post
title: "django-haystack 1.2.6 Release Notes"
date: 2011-12-09 10:29:54
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-haystack/django-haystack-1.2.6.tar.gz>

This release includes the following:

* I hate Python packaging.
* Made ``SearchIndex`` classes thread-safe. Thanks to craigds for the report & original patch.
* Added a couple more uses.
* Bumped reqs in docs for content extraction bits.
* Added a long description for PyPI.
* Solr backend support for rich-content extraction /  / This allows indexes to use text extracted from binary files as well / as normal database content. /  / Note: requires a very recent pysolr - see https://github.com/acdha/pysolr/tree/rich-content-extraction
* Fixed errant ``self.log``. /  / Thanks to terryh for the report!
