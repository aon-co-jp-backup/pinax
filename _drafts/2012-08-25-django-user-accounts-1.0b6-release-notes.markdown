---
layout: post
title: "django-user-accounts 1.0b6 Release Notes"
date: 2012-08-25 20:17:00
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-user-accounts/django-user-accounts-1.0b6.tar.gz>

This release includes the following:

* Bumped to 1.0b7
* Fixed bug with LogoutView.get_redirect_url /  / Needed to accept **kwargs and pass it on to default_redirect like the other / views and this fixes a NameError bug.
* Added signals documentation
* Add middleware installation instructions
