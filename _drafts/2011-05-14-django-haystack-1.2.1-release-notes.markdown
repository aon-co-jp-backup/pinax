---
layout: post
title: "django-haystack 1.2.1 Release Notes"
date: 2011-05-14 09:32:50
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-haystack/django-haystack-1.2.1.tar.gz>

This release includes the following:

* Fixed a typo in the autocomplete docs. Thanks to anderso for the catch!
* Fixed a backward-incompatible query syntax change Whoosh introduced between 1.6.1 & 1.6.2 that causes only one model to appear as though it is indexed.
* Updated AUTHORS to reflect the Kent's involvement in multiple index support.
* BACKWARD-INCOMPATIBLE: Added multiple index support to Haystack, which enables you to talk to more than one search engine in the same codebase. Thanks to: /  / * Kent Gormat for funding the development of this feature. / * alex, freakboy3742 & all the others who contributed to Django's multidb feature, on which much of this was based. / * acdha for inspiration & feedback. / * dcramer for inspiration & feedback. / * mcroydon for patch review & docs feedback. /  / This commit starts the development efforts for Haystack v2.
