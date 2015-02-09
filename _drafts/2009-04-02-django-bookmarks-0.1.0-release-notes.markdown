---
layout: post
title: "django-bookmarks 0.1.0 Release Notes"
date: 2009-04-02 01:59:22
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-bookmarks/django-bookmarks-0.1.0.tar.gz>

This release includes the following:

* added version number and code /  / git-svn-id: http://django-bookmarks.googlecode.com/svn/trunk@39 413268e4-d34f-0410-bd0d-61523dc7b0b6
* my attempt at making distutils-ready /  / git-svn-id: http://django-bookmarks.googlecode.com/svn/trunk@38 413268e4-d34f-0410-bd0d-61523dc7b0b6
* strip bookmark description field /  / git-svn-id: http://django-bookmarks.googlecode.com/svn/trunk@37 413268e4-d34f-0410-bd0d-61523dc7b0b6
* removed old migration management command /  / git-svn-id: http://django-bookmarks.googlecode.com/svn/trunk@36 413268e4-d34f-0410-bd0d-61523dc7b0b6
* added ability to delete bookmark instances /  / git-svn-id: http://django-bookmarks.googlecode.com/svn/trunk@35 413268e4-d34f-0410-bd0d-61523dc7b0b6
* added 'your bookmarks' view /  / git-svn-id: http://django-bookmarks.googlecode.com/svn/trunk@34 413268e4-d34f-0410-bd0d-61523dc7b0b6
* handle failed URL better /  / git-svn-id: http://django-bookmarks.googlecode.com/svn/trunk@33 413268e4-d34f-0410-bd0d-61523dc7b0b6
* fixed force_insert problem /  / git-svn-id: http://django-bookmarks.googlecode.com/svn/trunk@32 413268e4-d34f-0410-bd0d-61523dc7b0b6
* calculate bookmarklet address and pass in to template /  / git-svn-id: http://django-bookmarks.googlecode.com/svn/trunk@31 413268e4-d34f-0410-bd0d-61523dc7b0b6
* made __unicode__ of BookmarkInstance i18n aware /  / git-svn-id: http://django-bookmarks.googlecode.com/svn/trunk@30 413268e4-d34f-0410-bd0d-61523dc7b0b6
* tags field is no longer required /  / git-svn-id: http://django-bookmarks.googlecode.com/svn/trunk@29 413268e4-d34f-0410-bd0d-61523dc7b0b6
* tagging on bookmark instances (from Rajeev Sebastian) /  / git-svn-id: http://django-bookmarks.googlecode.com/svn/trunk@28 413268e4-d34f-0410-bd0d-61523dc7b0b6
* fix 500 when accessing bookmarks unauthenticated /  / git-svn-id: http://django-bookmarks.googlecode.com/svn/trunk@27 413268e4-d34f-0410-bd0d-61523dc7b0b6
* fixed problem with absent has_favicon /  / git-svn-id: http://django-bookmarks.googlecode.com/svn/trunk@26 413268e4-d34f-0410-bd0d-61523dc7b0b6
* added svn:ignore /  / git-svn-id: http://django-bookmarks.googlecode.com/svn/trunk@25 413268e4-d34f-0410-bd0d-61523dc7b0b6
* added message when bookmark saved /  / git-svn-id: http://django-bookmarks.googlecode.com/svn/trunk@24 413268e4-d34f-0410-bd0d-61523dc7b0b6
* fixed up newforms reference. /  / git-svn-id: http://django-bookmarks.googlecode.com/svn/trunk@23 413268e4-d34f-0410-bd0d-61523dc7b0b6
* Made changes to support new NFA version of trunk. /  / git-svn-id: http://django-bookmarks.googlecode.com/svn/trunk@22 413268e4-d34f-0410-bd0d-61523dc7b0b6
* include user's bookmarks in view so we can act on whether a bookmark has been saved by current user or not /  / git-svn-id: http://django-bookmarks.googlecode.com/svn/trunk@21 413268e4-d34f-0410-bd0d-61523dc7b0b6
* upgrade command for creating bookmark instances from bookmarks /  / git-svn-id: http://django-bookmarks.googlecode.com/svn/trunk@20 413268e4-d34f-0410-bd0d-61523dc7b0b6
* validate against the same user bookmarking same link twice /  / git-svn-id: http://django-bookmarks.googlecode.com/svn/trunk@19 413268e4-d34f-0410-bd0d-61523dc7b0b6
* more clean up in bookmark instances /  / git-svn-id: http://django-bookmarks.googlecode.com/svn/trunk@18 413268e4-d34f-0410-bd0d-61523dc7b0b6
* part 4 of per-user bookmark instances [brosner to the rescue] /  / git-svn-id: http://django-bookmarks.googlecode.com/svn/trunk@17 413268e4-d34f-0410-bd0d-61523dc7b0b6
* part 3 of per-user bookmark instances [still broken] /  / git-svn-id: http://django-bookmarks.googlecode.com/svn/trunk@16 413268e4-d34f-0410-bd0d-61523dc7b0b6
* part 2 of per-user bookmark instances [still broken] /  / git-svn-id: http://django-bookmarks.googlecode.com/svn/trunk@15 413268e4-d34f-0410-bd0d-61523dc7b0b6
* part 1 of having per-user bookmark instances [currently broken] /  / git-svn-id: http://django-bookmarks.googlecode.com/svn/trunk@14 413268e4-d34f-0410-bd0d-61523dc7b0b6
* Add feed support for bookmarks by ericfo /  /  / git-svn-id: http://django-bookmarks.googlecode.com/svn/trunk@13 413268e4-d34f-0410-bd0d-61523dc7b0b6
* fixed existence check of favicon -- was this even tested before? /  / git-svn-id: http://django-bookmarks.googlecode.com/svn/trunk@12 413268e4-d34f-0410-bd0d-61523dc7b0b6
* fixed redirect required bug /  / git-svn-id: http://django-bookmarks.googlecode.com/svn/trunk@11 413268e4-d34f-0410-bd0d-61523dc7b0b6
* Added False state to get_favicon_url /  /  / git-svn-id: http://django-bookmarks.googlecode.com/svn/trunk@10 413268e4-d34f-0410-bd0d-61523dc7b0b6
* Add favicons support /  /  / git-svn-id: http://django-bookmarks.googlecode.com/svn/trunk@9 413268e4-d34f-0410-bd0d-61523dc7b0b6
* added constraint on form field max length /  / git-svn-id: http://django-bookmarks.googlecode.com/svn/trunk@5 413268e4-d34f-0410-bd0d-61523dc7b0b6
* added svn:ignore /  / git-svn-id: http://django-bookmarks.googlecode.com/svn/trunk@4 413268e4-d34f-0410-bd0d-61523dc7b0b6
* added support for redirect on submission /  / git-svn-id: http://django-bookmarks.googlecode.com/svn/trunk@3 413268e4-d34f-0410-bd0d-61523dc7b0b6
* added initial app from Pinax /  / git-svn-id: http://django-bookmarks.googlecode.com/svn/trunk@2 413268e4-d34f-0410-bd0d-61523dc7b0b6
* Initial directory structure. /  / git-svn-id: http://django-bookmarks.googlecode.com/svn/trunk@1 413268e4-d34f-0410-bd0d-61523dc7b0b6
