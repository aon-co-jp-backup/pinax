---
layout: post
title: "django-announcements 0.1.1 Release Notes"
date: 2010-04-22 08:36:52
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-announcements/django-announcements-0.1.1.tar.gz>

This release includes the following:

* added LICENSE file
* Added fetch_announcements template tag
* Added .gitignore
* Style changes
* No longer needed with recent change making creator not editable in admin. /  / This reverts commit 407e2b0d5e4e359f99972e371af1e8e43bc08b4f.
* Merge commit 'richardbarran/master'
* pep8
* Limit the choices of creator to only staff members.
* Change 'creator' and 'creation_date' to be non-editable in the Admin, and instead populated automatically.
* The 'Send Now' field is not a real field; make this distinction (hopefully) clearer by moving it into its own fieldset in the admin form.
* Merge branch 'master' of git://github.com/brosner/django-announcements
* Correct some more misspellings of announcement(s). /  / Signed-off-by: Brian Rosner <brosner@gmail.com>
* Correct some more misspellings of announcement(s).
