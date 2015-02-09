---
layout: post
title: "django-user-accounts 1.0b15 Release Notes"
date: 2013-11-15 21:13:35
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-user-accounts/django-user-accounts-1.0b15.tar.gz>

This release includes the following:

* Bumped version for next release
* Updated classifiers
* Added some documentation on the new ACCOUNT_HOOKSET
* Added support for hook sets /  / These new hook sets is a very simple way of overriding functionality all over / the app. It requires no default configuration, but if you want to override some / functionality (initial email sending) you can define your own AccountHookSet / class and it will act as if your code is injected in DUA.
* Try to reverse the fallback url (like in `handle_redirect_to_login`)
* add Polish translations
* use hasAttr not in
* bump pytz and lint dict
* fwd and bkwd compatible form field ordering
* Provide a label for the email field
* Only allow get and post requests /  / Sometimes bots will hit this view with HEAD requests which / generates exceptions. This should enable Django to return / a proper HTTP response code saying that method is not allowed.
* Added EmailAddress to admin
* Blank lines should not contain any whitespace /  / Eldarion has decided for open source projects to conform to the blank lines / should not contain whitespace style guideline. While we still disagree with it, / we want to do less style guide enforcing with our contributors and make it / easier for them to contribute. /  / This does not mean we won't enforce this style guideline. Consistency is still / king and mixing whitespace lines with no whitespace lines is a big no-no. It / also still unacceptable to send us a pull request fixing two lines and / correcting whitespace in other parts of the code. Your pull requests should be / concise and not the product of a crazy editor that fixes all whitespace because / it thinks it is doing you a favor.
* added explicit LICENSE file
* Add Python 3 to package classifiers
* Simplified tests (for now; need to build out proper tests)
* Pinned django-nose in Travis YML
* Fixed exclusion to match
* Excluded 1.4.x from Python 3 builds
* Added Python 3.3 to Travis
* Added Travis and runtests.py
* Changed print usage to print function
* Fixed call to iteritems
* Officially support Python 3
* Added unicode_literals for better compatibility
* Fixed unicode problems on Python 3
* Ensure ACCOUNT_TIMEZONES is always a list
* Fixed urlparse for Python 3
* Switched to .format for string formatting
* Updated except syntax
