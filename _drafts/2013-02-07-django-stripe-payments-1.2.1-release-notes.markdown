---
layout: post
title: "django-stripe-payments 1.2.1 Release Notes"
date: 2013-02-07 04:03:14
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-stripe-payments/django-stripe-payments-1.2.1.tar.gz>

This release includes the following:

* 1.2.1 /  / Upgrade stripe library requirements
* Default current to USD /  / This enables the enhancement of making currency a setting / instead of being hard-coded, backwards compatible.
* Add support for changing currency in Settings /  / Stripe is now available in Canada so you are now able to choose to process in either American ("usd") and Canadian ("cad") currency. /  / At the moment, "usd" is hard-coded as the currency variable in several spots which causes errors if your account is set to "cad". These changes allow the currency to be set as one of the variables in PAYMENT_PLANS.
