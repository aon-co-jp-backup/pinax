---
layout: post
title: "django-user-accounts 1.0b18 Release Notes"
date: 2014-01-14 15:05:56
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-user-accounts/django-user-accounts-1.0b18.tar.gz>

This release includes the following:

* Moved to a stable classifier
* Bumped version for next release candidate, if needed
* Bumped version for first release candidate
* Added .gitignore
* Updated translations from Transifex /  / It appears some translations were lost due to them being handled outside of / Transifex. Can those responsible for those either help me move them over or / translate on Transifex.
* Updated transifex URL
* Updated translation source
* Removed unused imports and fixed User bug via pyflakes
* Added hook points for token creation /  / Fixes #77.
* Allow site to pass through to EmailConfirmation.send /  / Fixes #73.
* Added documentation around duplicate email storage /  / Fixes #54.
* Allow IntegrityError to propagate with duplicate email /  / Fixes #62. When ACCOUNT_EMAIL_UNIQUE is True we should fail loudly when an / attempt to insert a duplicate occurs. Let the callers handle the failure.
* Fixed missing account exception in TimezoneMiddleware /  / Fixes #79 and #80.
* Changed install_requires to allow newer versions /  / Fixes #101. This is not ideal because newer versions can cause future breakage, / but does allow for newer versions which do work to be installed in the / environment.
* Fixed use of reduce for Python 3.3+ /  / Fixes #100.
* Updated Django versions in .travis.yml
* Bumped version for next release
* Added support for customizable user models /  / DUA now supports Django 1.5 user models with compatibility to 1.4. Fixes #57. /  / Huge thanks to Filip Wasilewski (nigma) and Thomas Schreiber (rizumu) who helped / implement the feature.
* Fixed vertical whitespace in admin.py
* Updated pytz requirement
