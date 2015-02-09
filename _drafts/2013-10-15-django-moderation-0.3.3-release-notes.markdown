---
layout: post
title: "django-moderation 0.3.3 Release Notes"
date: 2013-10-15 12:14:26
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-moderation/django-moderation-0.3.3.tar.gz>

This release includes the following:

* Add option to not overwrite managers
* Add try/except on SerializedObjectField
* Remove leftover junk code
* Assign ModerationObjectManager classes, not instances, to models. Fixes related manager.
* Fix admin for approved objects
* Add docs about unapproved model instances on installation
* Update FilterSpec to ListFilter for Django 1.4
* Drop ModeratedObjectForm; add hack for django-reversion to continue to work
* Set Moderation Manager as _default_manager
* If not ModeratedObject found, default to not visible
* Do the TODO (make things actually work)
* Fix extra_context in 1.4
* Fixup tests for django 1.4
* Allow overriding form= as long as that form is a BaseModeratedObjectForm
* Disable custom ContentType filter for 1.4
* Convenient message for PEP8TestCase if pep8 is not installed.
* Fixed form initials for file/image fields.
* Add EditorConfig file for indentation and newlines
* Use tabs consistently for indentation in all HTML
