---
layout: post
title: "django-user-accounts 1.0.1 Release Notes"
date: 2014-12-18 18:24:10
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-user-accounts/django-user-accounts-1.0.1.tar.gz>

This release includes the following:

* Prepare for 1.0.1 release
* Style fix /  / [ci skip]
* Set env in exclude to match exactly
* Quote install to allow version specifiers
* Bumped version for next pre-release
* Fix logout on password change in Django 1.7+ /  / Fixes #143. /  / For more information: / https://docs.djangoproject.com/en/1.7/topics/auth/default/#session-invalidation-on-password-change
* Always test against latest point release
* Fix the search on EmailAddress admin. /  / We cannot query a foreign key directly, but we need to / specify one field. Now we query the username
* strip whitespace
