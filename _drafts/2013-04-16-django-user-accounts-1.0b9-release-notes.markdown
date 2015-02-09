---
layout: post
title: "django-user-accounts 1.0b9 Release Notes"
date: 2013-04-16 20:54:00
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-user-accounts/django-user-accounts-1.0b9.tar.gz>

This release includes the following:

* Bumped version
* Added complete sign up AJAX template support
* Added support for AJAX GET requests to log in and sign up /  / When a request comes in for the login or signup views, we will detect an AJAX / request and serve a different template.
* Forgot a missing return. :(
* Be more resilliant to auth backends that don't require username/password as the params.
* Fixed invalid signup code case to notify in all cases /  / When a signup code is invalid we will now issue a user message regardless of / the value for ACCOUNT_OPEN_SIGNUP.
* FR locale po metadata update
* Added fr locale
