---
layout: post
title: "django-stripe-payments 2.0b5 Release Notes"
date: 2013-03-25 16:49:35
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-stripe-payments/django-stripe-payments-2.0b5.tar.gz>

This release includes the following:

* 2.0b5
* Compare offset-naive with offset-naive, both in UTC
* Link customer before record_charge
* Update installation.rst /  / Fix a few typos and make a clear distinction between installation and configuration steps.
* Fix bug in history.html template
* Added Customer.charge and modified Customer.purchase /  / The charging aspect of Customer.purchase has been moved to Customer.charge and / Customer.purchase renamed to subscribe. This makes one-off charges simpler and / not all tied up with plan subscription. /  / BACKWARDS INCOMPATIBLE
* bumped version for next release
* Add LICENSE file /  / Closes #23
* 2.0b3
* Do not display the period on payment history template
* Add ability to sync customer data
* 2.0b2
* Add method for updating quantity on a subscription
* Update invoice email
* 2.0b1
* Update installation docs
* Update changelog
* Refactor models to be more in line with API changes
* Handle the transfer.updated webhook
* Add new event types to webhook signals
* Set the api version
* Set api_key once
