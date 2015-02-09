---
layout: post
title: "django-user-accounts 1.0b13 Release Notes"
date: 2013-05-30 21:31:18
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-user-accounts/django-user-accounts-1.0b13.tar.gz>

This release includes the following:

* Bumped version
* Cleaned up fallback URL behavior
* Changed default_redirect session behavior /  / Destroy the session variable after grabbing it from the session. This prevents / leaking the data to other requests.
* Changed variable name to be descriptive and not stomp on builtin
