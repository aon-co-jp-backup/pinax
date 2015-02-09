---
layout: post
title: "django-waitinglist 1.1 Release Notes"
date: 2013-12-20 12:56:23
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-waitinglist/django-waitinglist-1.1.tar.gz>

This release includes the following:

* update docs
* 1.1
* Merge branch 'master' into auth /  / Conflicts: / 	waitinglist/models.py / 	waitinglist/views.py
* use user permissions instead of is_staff to grant access to management views
* lint
* strip whitespace
* Update models.py /  / re-indent blank line as per contribution guidelines
* Slightly improve admin interface /  / Provide missing label for WaitingListEntry, which only becomes a problem in cases where an admin/staff needs to manually update a SUrveyInstance. /  / Previously the entry dropdown would only contain the values "WaitingListEntry object". /  / Now, it could contain the email address of the waitinglist object.
