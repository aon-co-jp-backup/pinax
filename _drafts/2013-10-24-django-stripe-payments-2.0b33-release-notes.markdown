---
layout: post
title: "django-stripe-payments 2.0b33 Release Notes"
date: 2013-10-24 21:00:44
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-stripe-payments/django-stripe-payments-2.0b33.tar.gz>

This release includes the following:

* 2.0b33
* added raw_id_fields to EventProcessingException admin
* bug fixed in installation.rst - Added missing comma in PAYMENTS_PLANS
* Formatting and lint fixes
* Merge branch 'master' of github.com:eldarion/django-stripe-payments into bug/credit-card-updates /  / Conflicts: / 	payments/tests/test_commands.py / 	payments/tests/test_customer.py / 	payments/tests/test_email.py
* Needed to put the warning suppression on the function line instead the statement where the delete takes place
* See if this satisfies the test matrix - removing warnings for statement
* Whoops - replacing disable-msg with disable
* Removing deprecation warnings for pylint
* Removing deprecation warnings (coming from pylint) and also altering the Meta warning to suppress for different versions of Python being used with pylint
* Disabling line too long for test module
* Disabling Meta class warning - not sure why this wasn't working before.: 'Old-style class defined.'
* Pylint lines too long fixes
* Fixing empty docstring
* Merge branch 'master' of github.com:eldarion/django-stripe-payments into bug/credit-card-updates
* Fixing bug where event signal handlers will still be able to access the old plan even after it has been deleted
* Sorting these in alphabetical order
* Changing the disconnect / connect signal handlers to not use weak references
* Fixing spelling mistakes
* Another lint bug: E125 continuation line does not distinguish itself from next logical line
* Fixing line too long lint error - LAME ;)
* Merge branch 'master' of github.com:eldarion/django-stripe-payments into bug/credit-card-updates
* Spelling error - also see this for how to patch settings in Django: /  / https://docs.djangoproject.com/en/1.5/topics/testing/overview/#overriding-settings
* Customer.sync Issue /  / Fixing bug where credit card does not get removed properly.  Also fixing issue with signal card_changed not getting sent when there is a card change whether it be removed or updated. /  / All of these fixes include tests.
* Removed extra closing td
* Missing closing div tag
* Break line in an odd place to keep the build from breaking.
* Added documentation example.
* Add trial period days option to initial plans.
* Update installation.rst /  / Fixed incorrect usage of specially.
* Sync attempt_count to attempts field on Invoice
* Added total_amount @property to CurrentSubscription model
