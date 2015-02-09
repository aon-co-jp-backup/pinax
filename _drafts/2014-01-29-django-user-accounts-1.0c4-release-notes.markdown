---
layout: post
title: "django-user-accounts 1.0c4 Release Notes"
date: 2014-01-29 18:14:53
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-user-accounts/django-user-accounts-1.0c4.tar.gz>

This release includes the following:

* Updated translations
* Bumped RC version
* Fixed circular reference madness with custom user models /  / This fixes #113 where a circular import can happen when populating the app / cache or the app cache isn't loaded yet.
* Update LICENSE year
