---
layout: post
title: "django-avatar 2.0 Release Notes"
date: 2013-09-13 16:54:39
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-avatar/django-avatar-2.0.tar.gz>

This release includes the following:

* Added post_delete signal to Avatar model in order to clean up the file system when AVATAR_MAX_AVATARS_PER_USER is equal to 1 or when Avatar instances are removed.  This functionality is controlled by the new AVATAR_CLEAN_REMOVED setting which is False by default.
* 2.0a2-eldarion
* Optional css_class passed as args to the avatar tag. /  / If no class is passed, no class is added.
* Add testdata to distribution package so third parties can run the tests
* Add ability to use https with gravatar
* Update messages so it's compatible with Django 1.4
* removed all dependence on django-notification and django-friends by changing to emitting signals
* master is now 2.0a1
* Bumped version.
* Added new AVATAR_DEFAULT_SIZE setting with a default of 80.
* Moved settings from avatar main module to own settings module and signal callback to models module to be able to prevent import errors in non-Django Python environments.
* Added README and update CONTRIBUTORS file.
* Bumped to 1.1a4.
* Added a few docstrings.
* Also invalidate the cache when deleting an avatar.
* Ignore all egg-info dirs.
* Added template tag caching (default timeout: 60 minutes) to template tags, includes invalidation.
* Merge branch 'master' of git://github.com/ericflo/django-avatar
