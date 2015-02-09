---
layout: post
title: "django-stripe-payments 2.0.0 Release Notes"
date: 2014-09-29 15:52:30
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-stripe-payments/django-stripe-payments-2.0.0.tar.gz>

This release includes the following:

* 2.0.0
* Use name of distribution not the name of the package
* pinax-starter-app reconciliation + Pinax ready
* Update tox envs for 1.7 release
* Updating test
* Capture the payment of an existing, uncaptured, charge.
* add the missing default to the correct field
* refs #129: add missing default to BooleanField
* coveralls: after_script -> after_success
* Remove redudant scripts for testing
* README: advise to use detox for tests
* 100% coverage for views.py
* travis-ci: use travis matrix with tox envs
* Initial support for py3k
* test_plans_create: dict doesn't preserve order
* Update .travis.yml to run tests with detox
* Add PyPi classifiers
* Add tox configuration matrix
* fix encoding issue on py3k during installation
* Remove dev_requirements.txt /  / Reasons: / - outdated packages (tests were failing) / - not tested (tox/travis-ci don't use this file) / - lots of unneeded packages for the project (ansible, gmp2, ...)
* Bump copyright date
* Fix up lint errors
* Modify flake command
* flake8 fixes
* added tox.ini with flake8 config
* removed --use-mirrors
* switched to flake8
* Update README.rst
* Patched ActiveSubscriptionMiddleware to support urls containing patterns
* Added a development requirements file for convenience
* Added .gitignore from https://github.com/github/gitignore/blob/master/Python.gitignore
* remove extraneous comma
* additional dependencies for running the tests /  / I was running through the README and I found that I needed a couple more packages in order to run the tests.
* Fixed rotate_token(request) error /  / The error is due to `request.META` is a `Mock` object.
* Added test cases for JPY currency (a kind of zero-decimal currency)
* Added support of multi-currencies
* Update README.rst /  / Added integration suggestions to the Readme.
* Merge branch 'master' into fix-admin-required-fields /  / Conflicts: / 	payments/models.py
* Enable users to save objects in admin
* Add support for Django 1.6 /  / Three changes required: /  /  - BooleanField no longer defaults to False /  - filter(date__month=..., date__day=...) is now timezone aware, so /    a timezone needs to be specified in the settings /  - it now seems to require pytz, probably because of timezone /    awareness
* Only update the card if there is such data /  / to let user subscribe to free plans without credit card infos
* Add send_receipt option to Customer.charge
* ensure all boolean fields have False as default, otherwise in Django 1.6 it will be None
