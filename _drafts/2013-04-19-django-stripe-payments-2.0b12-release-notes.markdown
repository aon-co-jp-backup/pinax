---
layout: post
title: "django-stripe-payments 2.0b12 Release Notes"
date: 2013-04-19 12:55:17
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-stripe-payments/django-stripe-payments-2.0b12.tar.gz>

This release includes the following:

* Use the defaulted value
* Removed the un-needed raise call
* Refactored code to avoid a deprecation warning in Python 2.7
* Fix manifest
* Broke up tests into modules
* Test can_charge
* Test customer delete is same as purge
* Test customer purge
* Decouple update_card from other activities /  / Should fix #33
* Disable R0924 check on PlanForm /  / This check fails on Django 1.4 but not Django 1.5
* Update code style violations
* Switch from pep8/pyflakes to pylint
* Update transfer object status to paid
* PEP8 fix /  / Fixed E711 comparison to None should be 'if cond is None:'
* Customer admin filter fix /  / A bug in the admin filter for customers made it seem like you didn't have any customers if all the current customers weren't subscribers yet.
* Improved create customer /  / Made it so if the current user doesn't have a stripe customer associated with their account it will create one when they subscribe to a plan. This removes the need for running the init_customers management command when adding django-strip-payments to an existing project.
* Updated the subscribe.html template to give the user a friendlier message if they've already subscribed to a plan.
* More PEP8 fixes
* Wrapped text to comply with PEP8 E501
* Removed the need for payments.context_processors by adding a PaymentsContextMixin which has been added to all views that need it.
* Added title blocks to the default templates
* Add Checkout.js example
* Properly case the settings.py reference
* Add mock to the list of requirements for tests
* Fix deprecation warning re: urls.defaults /  / Thanks, Fred Palmer (https://github.com/fredpalmer)
* Switch to request.body for Django 1.5 compatibility /  / Thanks, Fred Palmer (https://github.com/fredpalmer), / for the patch.
* Add test to exercise webhook
* Update Travis Image
* Drop Python 3 targets for now /  / There seems to be something about the packaging/setup / that breaks in Python 3 environments.
* Drop support for 2.6
* PEP8 Fixes
* Fix travis config
* Fix Travis CI image
* Fix readme formatting
* Fix readme formatting
* Add travis integration
* Fix single-quotes
* Add some more tests to validate customer linking
* Add a test runner
* Add note about running test suite
* Remove lame print statement
* Start a test suite
* 2.0b12
* Fixed a bug that happens when subscription is None
* 2.0b11
* Upgrade to be compatible with Django 1.5
