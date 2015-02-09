---
layout: post
title: "django-stripe-payments 2.0b27 Release Notes"
date: 2013-08-20 00:29:26
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-stripe-payments/django-stripe-payments-2.0b27.tar.gz>

This release includes the following:

* Update subscription status template to handle cancel better
* 2.0b27
* Fix bug in subscription status template /  / Fixes #85
* Add some tests for some of the AJAX views
* Remove unused context variables
* Expect stripe_token to be there /  / If stripe_token wasn't there it was going to blow / up on an undefined error for the `data` variable. / This way the code is simpler.
* Expect the request to be AJAX /  / We don't have a return condition if it isn't AJAX / so for now just expect it. It would have blown up / either way, but at least now the code is simpler.
* Add requirements for tests
* Lint fix
* Add some view tests
* Test for all branching in convert_tstamp
* A silly little test to fully cover the settings module
* Add tests for template tags
* Clean up lints
* Fix bug in middleware that occurs when a user does not have a customer
* Add tests for middleware
* Add tests for ChargeManager
* Add test for sync_customers command
* Fix lint error
* Add tests to for init_plans and fix bugs identified through tests
* Add test for init_customers
* Clean up for consistent use of relative imports
* Add some settings to validate some of the settings.py
* Add tests for plan_from_stripe_id
* Move utility functions into a utils.py module
* No need to test admin.py so exclude from coverage
* Remove context processor /  / This is a backwards incompatible change in that if / you have the processor installed in settings.py / you will need to remove it, however, all views now / include this context. /  / If you have written you own custom views and are / relying on the context processor to put values in / context, you'll need to update your views.
* Use .coveragerc file /  / Want to eliminate coverage for tests that I include / in the payments package.
* Add coverage reporting
