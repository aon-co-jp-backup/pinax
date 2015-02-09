---
layout: post
title: "django-user-accounts 1.0c2 Release Notes"
date: 2014-01-16 17:42:40
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-user-accounts/django-user-accounts-1.0c2.tar.gz>

This release includes the following:

* Bumped version for next RC
* Added support for authentication backends on sign up /  / If you use custom authentication backends you may experience buggy behavior on / Django 1.6+. This commit allows you to turn on proper authentication backend / lookup for auto-login after sign up. /  / See FAQ for more information.
