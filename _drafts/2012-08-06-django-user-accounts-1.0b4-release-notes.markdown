---
layout: post
title: "django-user-accounts 1.0b4 Release Notes"
date: 2012-08-06 22:24:50
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-user-accounts/django-user-accounts-1.0b4.tar.gz>

This release includes the following:

* Updated pytz to latest
* Updated version to reflect next release
* Fix typo in previous bug fix
* Fix undefined variable bug in login_user
* BI: no longer pass new_user around to SignupView methods /  / Unified the API in SignupView to use self.created_user over passing new_user / around. self state is per-request and it keeps everything clean. Even though / this is may be less explicit, it is more inline with the design decisions of / class-based views.
* Set new_user on SignupView as created_user /  / This allows other methods that don't typically have access to the sign up / process to get at the created User instance. For example, get_success_url / might want to do a redirect based on this user.
