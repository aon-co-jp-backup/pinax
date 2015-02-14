---
layout: post
title: "django-mailer 0.1.0 Release Notes"
date: 2009-08-23 14:47:11
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-mailer/django-mailer-0.1.0.tar.gz>

This release includes the following:

* Call force_unicode on message when sending
* Encode unicode string before logging it
* Truncate subjects to fit in 100 character limit for database
* Added a back-reference to the Pinax deployment task that runs send_mail
