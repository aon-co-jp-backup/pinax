---
layout: post
title: "django-user-accounts 1.0b5 Release Notes"
date: 2012-08-21 22:01:33
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-user-accounts/django-user-accounts-1.0b5.tar.gz>

This release includes the following:

* Bumped version to reflect the current state
* Bumped version for next release
* Removed @@@ more comment from SQL migration
* Updated installation docs /  / Improved the pip install command and added django.contrib.sites to the / dependancies.
* Added Account model to admin.py /  / Account will now show up in the Django admin interface. /  / Fixes #28 — thanks to Douglas Meehan for the issue report.
* Fixed TimezoneMiddleware to handle empty account.timezone /  / It is possible for account.timezone to be empty which should fall back to / settings.TIME_ZONE. /  / Fixes #36 — thanks to Filip Wasilewski for the issue report.
* Changed import to use Django version for 2.6 /  / importlib is available on 2.7+ and we would like to maintain support for 2.6. /  / Fixes #39 — thanks to millerc for the issue report.
* Fixed redirect_field_name handling in views /  / Support for a custom redirect_field_name was lacking and needed a bit of / improvement. All views which support custom redirects using default_redirect / now correctly honour a custom field name and value from GET or POST. /  / Fixes #41 — thanks to Ben Lopatin for the issue report and initial code.
