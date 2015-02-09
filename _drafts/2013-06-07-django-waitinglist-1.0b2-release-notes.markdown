---
layout: post
title: "django-waitinglist 1.0b2 Release Notes"
date: 2013-06-07 16:40:14
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-waitinglist/django-waitinglist-1.0b2.tar.gz>

This release includes the following:

* Add some signals for waitinglist list entry and survey answering
* Small bits of clean up
* 1.0b2
* Make compatible with Django 1.5
* Add view to fill out surveys
* Update tests for value_choices change
* Remove choices m2m and just use value field
* Add admin for surveys
* Tests to validate survey logic
* Core modeling/functionality of a survey system
* Added CONTRIBUTING documentation to repository
* Break out ajax into a different view/url
* handle invalid form in ajax case
* Ship with a template
* Add ajax support
* Fail silently if an invalid code is used
* fixed signup code lookup during signup
* fixed form field signup_code to code
* fixed bug with SignupCode.create parameters
* fixed old url names used in redirect
* Fix use of namedtuples
* Fixed some bugs
* Fix missing import bug by using render instead of render_to_response
* started documentation; incomplete
* fixed README description
* updated description
* simplified `waitinglist_entry_form` with assignment_tag
* fixed receiver bits in models.py
* added cohort support
* added django-user-accounts to requirements
* Django 1.4 updates
* Port of pinax.apps.waitinglist
* removed egg-info directory and added .gitignore
* initial commit
