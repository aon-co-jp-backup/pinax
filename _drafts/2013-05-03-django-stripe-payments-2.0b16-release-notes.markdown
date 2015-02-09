---
layout: post
title: "django-stripe-payments 2.0b16 Release Notes"
date: 2013-05-03 14:19:24
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-stripe-payments/django-stripe-payments-2.0b16.tar.gz>

This release includes the following:

* bumped version for next release
* updated management commands to use format and fixed 2.6 support
* Ignore unused variable 'args'
* Bump version for next release
* Convert decimal dollars into integer cents for Customer.charge() /  / Everywhere else in DSP we pull integer cents amounts / from the API and convert them into decimal dollars. / This was the only place where we were breaking from / that pattern and so it is best if we update to be / consistent and only expect/accept decimal amounts.
