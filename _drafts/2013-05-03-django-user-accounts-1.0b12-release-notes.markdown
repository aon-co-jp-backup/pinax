---
layout: post
title: "django-user-accounts 1.0b12 Release Notes"
date: 2013-05-03 17:52:58
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-user-accounts/django-user-accounts-1.0b12.tar.gz>

This release includes the following:

* Bumped version for next release
* Fixed email confirmation logic /  / This commit prevents the User object from being marked inactive in cases where / an email address is verified by some other means than email confirmation.
* Merge branch 'master' of git://github.com/pinax/django-user-accounts into south
* Added support for south
* German Translation /  / German Translation Files
* Fix naive DateTimeField Warning /  / Set timezone.now as default value in Signupcoderesult
