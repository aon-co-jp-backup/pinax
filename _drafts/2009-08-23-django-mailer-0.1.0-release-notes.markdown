---
layout: post
title: "django-mailer 0.1.0 Release Notes"
date: 2009-08-23 14:47:11
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-mailer/django-mailer-0.1.0.tar.gz>

This release includes the following:

* modified classifier to indicate beta
* 0.1.0 final version
* force_unicode on message when sending
* encode unicode string before logging it
* Merge commit 'jtauber/master'
* Truncate subjects to fit in 100 character limit for database /  / Credit goes to Carl Meyer for originally reporting this
* Added a back-reference to the Pinax deployment task regarding running send_mail. /  / Signed-off-by: James Tauber <jtauber@jtauber.com>
