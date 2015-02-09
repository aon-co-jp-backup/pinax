---
layout: post
title: "django-stripe-payments 2.0b24 Release Notes"
date: 2013-08-14 03:46:19
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-stripe-payments/django-stripe-payments-2.0b24.tar.gz>

This release includes the following:

* 2.0b24
* Fix bug in another customer user model enhancement
* Wrap things up in functions to keep things tidy
* Fix bug with misnamed function
* These fields are more readable slightly longer than 80 characters
* Summary data on transfers is not always present /  / If the status of a transfer.created webhook is / "pending" then the summary information will be / missing.
* Fix copy and paste error
* Adding note about running lint script
* Fix typo in template
* Styles fixes
* Fixes a potential issue if trying to add payments before the app where the custom User model is defined in the app caching
* Add CONTRIBUTING document
* Attempt to fix travis
* Add a .gitignore
* Add script to run tests and coverage
* Blank lines should not contain any whitespace /  / Eldarion has decided for open source projects to conform to the blank lines / should not contain whitespace style guideline. We want to do less style guide enforcing with our contributors and make it easier for them to contribute. /  / This does not mean we won't enforce this style guideline. Consistency is still / king and mixing whitespace lines with no whitespace lines is discouraged.
* Extend the stripe_id fields to 255 characters /  / There was an announcement on the Stripe API mailing / list that they would be extending beyond 30 chars / soon. /  / Stripe hadn't previously picked a hard limit that / was published externally but after looking at IDs / I decided to make it a bit bigger than what I was / seeing and picked an arbitrary "50" for the length. /  / Stripe has committed to keeping it less than 50 for / at least the next 6 months and beyond that they are / committing to keeping them less than 255 characters. /  / See http://bit.ly/19cu4w8 for more details.
* Style cleanup
* Merged upsteram master and fixed positional argument string formatting
* Fixed bug in search field names for Customer admin
* Pin pylint to 0.27.0
* Fix bug where list wasn't getting extended
* Clean up style
* Merge branch 'subscription-cancellation-cleanup' of github.com:OysterBooks/django-stripe-payments into OysterBooks-subscription-cancellation-cleanup /  / Conflicts: / 	payments/models.py
* Merge branch 'custom-user-model-admin-fix' of github.com:OysterBooks/django-stripe-payments into OysterBooks-custom-user-model-admin-fix /  / Conflicts: / 	payments/__init__.py / 	payments/models.py
* Merge branch 'configurable-email-receipts' of github.com:OysterBooks/django-stripe-payments into OysterBooks-configurable-email-receipts /  / Conflicts: / 	payments/models.py
* Merge branch 'sync-deleted-subscription-fix' of github.com:OysterBooks/django-stripe-payments into OysterBooks-sync-deleted-subscription-fix /  / Conflicts: / 	payments/models.py
* Merge branch 'master' of github.com:eldarion/django-stripe-payments
* Delete CurrentSubscription when syncing with Stripe if it has been deleted in Stripe
* Make stripe_id non-unique for an InvoiceItem
* Fixed whitespace issues
* Fixed whitepsace issues
* Fix whitespace issues
* Make sending email receipts configurable
* Fixed admin to work with Django 1.5 custom User models that don't have a username or email field
* Added a  field to CurrentSubscription and updated the  method to properly check the status, cancel_at_period_end, and current_period_end flags.
* Linter disable
* Convert to django 1.5 custom models
* Update url to eldarion-ajax
* Add more info about eldarion-ajax to the docs /  / I missed the section on eldarion-ajax because I skipped over it thinking it had to do with bootstrap which I'm not using.  This makes it clearer.
