---
layout: post
title: "django-notification 1.1 Release Notes"
date: 2013-07-08 16:44:02
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-notification/django-notification-1.1.tar.gz>

This release includes the following:

* 1.1
* added the create_notice_type wrapper in models /  / In the docs it is advised to use create_notice_type to create a new NoticeType object. But this function was absent. Although it is possible to create a new NoticeType using the 'create' function of the class, this addition makes the code follow the docs and compatible with previous code and other apps.
* russian locale added
* Update readme with travis build info
* Clean up of code per pylint warnings
* Customize pylintrc for this project
* Add travis baseline
* Removed an errant backtick.
* Added CONTRIBUTING documentation to repository
