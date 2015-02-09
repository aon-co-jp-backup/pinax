---
layout: post
title: "django-stripe-payments 1.0 Release Notes"
date: 2012-10-23 13:55:53
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-stripe-payments/django-stripe-payments-1.0.tar.gz>

This release includes the following:

* Update README.rst
* 1.0
* Check for status on is_valid()
* Fix up rest of docs; for a first draft at least
* Fix bug in context processor
* 1.0.dev1
* 0.1.dev27 /  / Fixed bug
* 0.1.dev26
* Add transfer processing
* Fetch subscription status when an invoice is paid
* Add property for fetching a stripe customer object
* 0.1.dev25
* added subscription status to templates
* 0.1.dev24
* Enable overriding the PlanForm
* 0.1.dev23
* Add a can_charge method to Customer
* Current subscription should return the latest always
* 0.1.dev22
* Fix up subscribe functionality
* 0.1.dev21
* Handle null charges better
* 0.1.dev20
* Only purchase a plan if there is a trial period
* 0.1.dev19
* A subscription is valid if the period is current /  / If you care about the status in addition to period, then / that should result in an extra check at the site level
* 0.1.dev18
* Add cancelled and card_changed signals
* Remove print statement
* 0.1.dev17
* Add ability to purge customers but retain transaction data
* Sometimes there is not a charge element
* 0.1.dev16
* Handle duplicate events
* 0.1.dev15
* Inform the customer they do not have a card on file
* 0.1.dev14
* Made email template extensible
* 0.1.dev13
* Allow for overriding of how the customer name is displayed
* Use plan name instead of description
* 0.1.dev12
* Comply with ajax response
* 0.1.dev11
* Fix definition of is_active
* 0.1.dev10
* Add some display methods
* Order by date descending
* Remove unused code
* Prevent duplicate subscription records
* Require login on all direct_to_template views
* 0.1.dev9
* Reinitialize payment tag upon ajax refresh
* Add payment tag to subscription form
* Add "lead" subtitles to be consistent across templates
* Consolidate forms /  / This also passed in the form to the subscription / template which had been a bug up until now.
* 0.1.dev8
* Display stripe error messages to user
* Handle case where one of the fields isn't in the response
* 0.1.dev7
* 0.1.dev6
* 0.1.dev5
* Do not link customer on plan events
* 0.1.dev4
* Add a callback to facilitate site definition of per user trial_end setting
* Change param name to reflect what it really is
* Convert to timezone aware dates
* 0.1.dev3
* Add trial period support
* 0.1.dev2
* Get management functions working
* 0.1.dev1
