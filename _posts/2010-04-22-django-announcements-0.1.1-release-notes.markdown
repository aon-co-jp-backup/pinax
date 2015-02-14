---
layout: post
title: "django-announcements 0.1.1 Release Notes"
date: 2010-04-22 08:36:52
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-announcements/django-announcements-0.1.1.tar.gz>

This release includes the following:

* added LICENSE file
* added `fetch_announcements` template tag
* style changes
* reverted making creator non-editable in admin
* lint cleanup
* limit the choices of creator to only staff members.
* populate 'creator' and 'creation_date' automatically and make non-editable
* move send_now to it's own fieldset in admin to indicate it is not a real field
* correct misspellings of announcement(s).
