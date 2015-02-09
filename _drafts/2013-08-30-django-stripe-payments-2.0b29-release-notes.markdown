---
layout: post
title: "django-stripe-payments 2.0b29 Release Notes"
date: 2013-08-30 22:08:43
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-stripe-payments/django-stripe-payments-2.0b29.tar.gz>

This release includes the following:

* 2.0b31
* Fix bug where current period end wasn't getting recorded on cancel
* Only pay invoice if there is an amount due
* 2.0b30
* Pass in the customer object to cut down on an API call
* 2.0b29
* Enable creation of customer with card and plan
* Trial end is based on UTC not local timezone
