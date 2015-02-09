---
layout: post
title: "django-announcements 0.1.0 Release Notes"
date: 2009-01-05 02:47:13
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-announcements/django-announcements-0.1.0.tar.gz>

This release includes the following:

* Added PyPI classifiers. /  / git-svn-id: https://django-announcements.googlecode.com/svn/trunk@49 4e50ab13-fc4d-0410-b010-e1608ea6a288
* Hooked up the README file into long_description. /  / git-svn-id: https://django-announcements.googlecode.com/svn/trunk@48 4e50ab13-fc4d-0410-b010-e1608ea6a288
* Added a README file. /  / git-svn-id: https://django-announcements.googlecode.com/svn/trunk@47 4e50ab13-fc4d-0410-b010-e1608ea6a288
* Added in version info and prep for 0.1.0 final release. /  / git-svn-id: https://django-announcements.googlecode.com/svn/trunk@46 4e50ab13-fc4d-0410-b010-e1608ea6a288
* Added a MANIFEST.in file. /  / git-svn-id: https://django-announcements.googlecode.com/svn/trunk@45 4e50ab13-fc4d-0410-b010-e1608ea6a288
* Added an AUTHORS file. /  / git-svn-id: https://django-announcements.googlecode.com/svn/trunk@44 4e50ab13-fc4d-0410-b010-e1608ea6a288
* Switch to using distutils from setuptools. /  / git-svn-id: https://django-announcements.googlecode.com/svn/trunk@43 4e50ab13-fc4d-0410-b010-e1608ea6a288
* Added a template snippet for using site_wide_announcements variable from the context processor. /  / git-svn-id: https://django-announcements.googlecode.com/svn/trunk@42 4e50ab13-fc4d-0410-b010-e1608ea6a288
* Corrected some common misspellings of announcement(s). /  / git-svn-id: https://django-announcements.googlecode.com/svn/trunk@41 4e50ab13-fc4d-0410-b010-e1608ea6a288
* Added pretty complete documentation. /  / git-svn-id: https://django-announcements.googlecode.com/svn/trunk@40 4e50ab13-fc4d-0410-b010-e1608ea6a288
* Added a setup.py file. /  / git-svn-id: https://django-announcements.googlecode.com/svn/trunk@39 4e50ab13-fc4d-0410-b010-e1608ea6a288
* renamed notification templates /  / git-svn-id: https://django-announcements.googlecode.com/svn/trunk@38 4e50ab13-fc4d-0410-b010-e1608ea6a288
* Use the new interface to notification.send to explicitly override the default behavior and queue notifications for announcements. /  / git-svn-id: https://django-announcements.googlecode.com/svn/trunk@37 4e50ab13-fc4d-0410-b010-e1608ea6a288
* Added Python 2.3 support. /  / git-svn-id: https://django-announcements.googlecode.com/svn/trunk@36 4e50ab13-fc4d-0410-b010-e1608ea6a288
* Corrected a typo in athe admin form name. /  / git-svn-id: https://django-announcements.googlecode.com/svn/trunk@35 4e50ab13-fc4d-0410-b010-e1608ea6a288
* Added the ability for the user to control when the announcement is sent out to the users. This decouples it from the Announcement.save method. /  / git-svn-id: https://django-announcements.googlecode.com/svn/trunk@34 4e50ab13-fc4d-0410-b010-e1608ea6a288
* Make use of the new notification.queue since announcements deals with sending a notification to large amounts of users. /  / git-svn-id: https://django-announcements.googlecode.com/svn/trunk@33 4e50ab13-fc4d-0410-b010-e1608ea6a288
* Fix for backward incompatible change in django-notifications. issue_notice -> on_site. /  / git-svn-id: https://django-announcements.googlecode.com/svn/trunk@32 4e50ab13-fc4d-0410-b010-e1608ea6a288
* fixed force_insert problem /  / git-svn-id: https://django-announcements.googlecode.com/svn/trunk@31 4e50ab13-fc4d-0410-b010-e1608ea6a288
* Updated to use new signals code in Django. Thanks dougn for catching this. /  / git-svn-id: https://django-announcements.googlecode.com/svn/trunk@30 4e50ab13-fc4d-0410-b010-e1608ea6a288
* Fixed up project to be compatible with NFA version of trunk. /  / git-svn-id: https://django-announcements.googlecode.com/svn/trunk@29 4e50ab13-fc4d-0410-b010-e1608ea6a288
* initial pass at port to new notification templates -- plain.txt only now and no extra information beyond old notification messages yet /  / git-svn-id: https://django-announcements.googlecode.com/svn/trunk@28 4e50ab13-fc4d-0410-b010-e1608ea6a288
* Added a bunch of docstrings and improved existing ones. /  /  / git-svn-id: https://django-announcements.googlecode.com/svn/trunk@25 4e50ab13-fc4d-0410-b010-e1608ea6a288
* changed name of atom module to avoid name clash with gdata /  / git-svn-id: https://django-announcements.googlecode.com/svn/trunk@22 4e50ab13-fc4d-0410-b010-e1608ea6a288
* Fixed a minor typo in Announcement.save. Thanks rotlaus. /  /  / git-svn-id: https://django-announcements.googlecode.com/svn/trunk@21 4e50ab13-fc4d-0410-b010-e1608ea6a288
* When in DEBUG mode only send to staff members. This fixes an immediate problem, / but needs to be done with a bit more control. /  /  / git-svn-id: https://django-announcements.googlecode.com/svn/trunk@20 4e50ab13-fc4d-0410-b010-e1608ea6a288
* Use the proper namespace name for notificiation. /  /  / git-svn-id: https://django-announcements.googlecode.com/svn/trunk@19 4e50ab13-fc4d-0410-b010-e1608ea6a288
* Fixed a couple more typos that prevented notifications to be sent. /  /  / git-svn-id: https://django-announcements.googlecode.com/svn/trunk@18 4e50ab13-fc4d-0410-b010-e1608ea6a288
* Fixed a typo in an import. /  /  / git-svn-id: https://django-announcements.googlecode.com/svn/trunk@17 4e50ab13-fc4d-0410-b010-e1608ea6a288
* Added django-notification support. When announcements are created they are / sent as a notification to registered users. django-notification handles the / settings on whether the user wants to recieve them or not. /  /  / git-svn-id: https://django-announcements.googlecode.com/svn/trunk@16 4e50ab13-fc4d-0410-b010-e1608ea6a288
* Added back Announcement in views.py imports. Didn't mean to take it out. /  /  / git-svn-id: https://django-announcements.googlecode.com/svn/trunk@15 4e50ab13-fc4d-0410-b010-e1608ea6a288
* Refactor a few things. Added tests. /  /     - Extracted the request from the manager. /     - Created a helper function to deal with request based announcement filtering. /     - Changed the session variable name from announcements_hidden to excluded_announcements /  /  / git-svn-id: https://django-announcements.googlecode.com/svn/trunk@14 4e50ab13-fc4d-0410-b010-e1608ea6a288
* added svn:ignore /  / git-svn-id: https://django-announcements.googlecode.com/svn/trunk@13 4e50ab13-fc4d-0410-b010-e1608ea6a288
* i18n'ifed the Announcement model. /  /  / git-svn-id: https://django-announcements.googlecode.com/svn/trunk@12 4e50ab13-fc4d-0410-b010-e1608ea6a288
* Added a default value to creation_date in Announcement to be the current datetime. /  /  / git-svn-id: https://django-announcements.googlecode.com/svn/trunk@11 4e50ab13-fc4d-0410-b010-e1608ea6a288
* Perform a redirect to the next GET variable. /  /  / git-svn-id: https://django-announcements.googlecode.com/svn/trunk@10 4e50ab13-fc4d-0410-b010-e1608ea6a288
* Added site-wide announcements. /  /  / git-svn-id: https://django-announcements.googlecode.com/svn/trunk@9 4e50ab13-fc4d-0410-b010-e1608ea6a288
* Removed a bit of debugging. /  /  / git-svn-id: https://django-announcements.googlecode.com/svn/trunk@8 4e50ab13-fc4d-0410-b010-e1608ea6a288
* Added the ability to send members only annoucements. /  /  / git-svn-id: https://django-announcements.googlecode.com/svn/trunk@7 4e50ab13-fc4d-0410-b010-e1608ea6a288
* Fixed some typos. Added the ability to hide announcements on a per request basis. /  /  / git-svn-id: https://django-announcements.googlecode.com/svn/trunk@6 4e50ab13-fc4d-0410-b010-e1608ea6a288
* Added a urls.py and fixed Announcement.get_absolute_url to use reverse. /  /  / git-svn-id: https://django-announcements.googlecode.com/svn/trunk@5 4e50ab13-fc4d-0410-b010-e1608ea6a288
* Renamed NewsItem -> Announcment /  /  / git-svn-id: https://django-announcements.googlecode.com/svn/trunk@4 4e50ab13-fc4d-0410-b010-e1608ea6a288
* Trunkified the NewsItem model. /  /  / git-svn-id: https://django-announcements.googlecode.com/svn/trunk@3 4e50ab13-fc4d-0410-b010-e1608ea6a288
* initial check in of previous code /  / git-svn-id: https://django-announcements.googlecode.com/svn/trunk@2 4e50ab13-fc4d-0410-b010-e1608ea6a288
* Initial directory structure. /  / git-svn-id: https://django-announcements.googlecode.com/svn/trunk@1 4e50ab13-fc4d-0410-b010-e1608ea6a288
