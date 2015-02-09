---
layout: post
title: "django-notification 1.0 Release Notes"
date: 2013-01-14 17:59:58
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-notification/django-notification-1.0.tar.gz>

This release includes the following:

* 1.0
* Update docs /  / Moved and updated CHANGELOG to be a part of the / documentation. Also, updated the settings docs / to include missing settings that were previously / undocumented.
* Remove captureas tag /  / This is no longer needed as Django now supports / creating assignment tags
* Style nit
* Do not import *
* Remove tests that do not test anything /  / All this one test tests is that the model API works / which isn't specific to this app. Better to remove / this for now and add proper tests later that actually / test/validate something in this app.
* Add notice_settings.html template
* Make url tag compatible with Django 1.5
* Fix style nit
* Clean up imports in engine.py
* Remove unused message.py module
* Start sections to document CHANGELOG
* Update AUTHORS
* Replace '_' with '/' in example file path.
* Add missing signals import.
* Remove unused import/code
* Use cPickle only /  / I am not 100% clear on why the fallback to pickle / as I think cPickle is pretty much available in / modern Python versions.
* Fix a style nit
* Remove unused decorators.py module
* Remove extraneous code /  / The get_notification_setting function was not / needed anymore as there was identical functionality / as a class method on the NoticeSetting model. /  / In addition to this fix, the import * was / removed for a more explicit import list
* Initial 1.0 commit
