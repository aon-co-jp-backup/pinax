---
layout: post
title: "django-avatar 1.0.0 Release Notes"
date: 2008-10-28 09:51:53
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-avatar/django-avatar-1.0.0.tar.gz>

This release includes the following:

* Added setup.py /  / git-svn-id: http://django-avatar.googlecode.com/svn/trunk@34 c76b2324-5f53-0410-85ac-b1078a54aeeb
* Added inital pass of documentation. /  / git-svn-id: http://django-avatar.googlecode.com/svn/trunk@33 c76b2324-5f53-0410-85ac-b1078a54aeeb
* Slightly shallower resized image paths. /  / git-svn-id: http://django-avatar.googlecode.com/svn/trunk@32 c76b2324-5f53-0410-85ac-b1078a54aeeb
* Thanks for the help, PyFlakes. /  / git-svn-id: http://django-avatar.googlecode.com/svn/trunk@31 c76b2324-5f53-0410-85ac-b1078a54aeeb
* Completely refactored this package so that it no longer references the local filesystem.  The API has been simplified and it has been tested with both file system backends and S3 backends.  Gearing up for the first official release. /  / git-svn-id: http://django-avatar.googlecode.com/svn/trunk@30 c76b2324-5f53-0410-85ac-b1078a54aeeb
* Made all imports relative and cleaned up the imports in general.  Thanks, PyFlakes! /  / git-svn-id: http://django-avatar.googlecode.com/svn/trunk@29 c76b2324-5f53-0410-85ac-b1078a54aeeb
* fixed force_insert problem /  / git-svn-id: http://django-avatar.googlecode.com/svn/trunk@28 c76b2324-5f53-0410-85ac-b1078a54aeeb
* Removed the import_gravatars script as it no longer worked properly.  This may be re-written at some point, but right now it is just cruft. /  / git-svn-id: http://django-avatar.googlecode.com/svn/trunk@27 c76b2324-5f53-0410-85ac-b1078a54aeeb
* Changed the max_length of the avatar ImageField, as we were seeing some errors about the path being too short. /  / git-svn-id: http://django-avatar.googlecode.com/svn/trunk@26 c76b2324-5f53-0410-85ac-b1078a54aeeb
* Added management command to rebuild avatars.  This is useful for when an administrator wishes to change the size of the auto-generated avatar sizes. /  / git-svn-id: http://django-avatar.googlecode.com/svn/trunk@25 c76b2324-5f53-0410-85ac-b1078a54aeeb
* Made avatar selection more clear by providing initial data for the form. /  / git-svn-id: http://django-avatar.googlecode.com/svn/trunk@24 c76b2324-5f53-0410-85ac-b1078a54aeeb
* Fixed problem with uploading .GIF files, as they need to be conditionally converted to RGB. /  / git-svn-id: http://django-avatar.googlecode.com/svn/trunk@23 c76b2324-5f53-0410-85ac-b1078a54aeeb
* Got rid of two print statements that could cause mod_wsgi to error out. /  / git-svn-id: http://django-avatar.googlecode.com/svn/trunk@22 c76b2324-5f53-0410-85ac-b1078a54aeeb
* Fixed pathing to the mkdirs call. /  / git-svn-id: http://django-avatar.googlecode.com/svn/trunk@21 c76b2324-5f53-0410-85ac-b1078a54aeeb
* Modified the rest of the module to be able to make use of the new added flexibility of the non-gravatar interface. /  / git-svn-id: http://django-avatar.googlecode.com/svn/trunk@20 c76b2324-5f53-0410-85ac-b1078a54aeeb
* Completely refactored this module.  The model has been changed to reflect more sane defaults.  A new set of templatetags have been created as well, however, the gravatar public API has been preserved.  The only thing that still needs to be done is to rewrite the administrative views for uploading/deleting/changing avatars. /  / git-svn-id: http://django-avatar.googlecode.com/svn/trunk@19 c76b2324-5f53-0410-85ac-b1078a54aeeb
* fixed signal typo /  / git-svn-id: http://django-avatar.googlecode.com/svn/trunk@18 c76b2324-5f53-0410-85ac-b1078a54aeeb
* Updated django-avatar to use the new signals stuff. /  / git-svn-id: http://django-avatar.googlecode.com/svn/trunk@17 c76b2324-5f53-0410-85ac-b1078a54aeeb
* Added caching. /  / git-svn-id: http://django-avatar.googlecode.com/svn/trunk@16 c76b2324-5f53-0410-85ac-b1078a54aeeb
* Handle the MultipleObjectsReturned edge case (shouldn't happen, but it might) /  / git-svn-id: http://django-avatar.googlecode.com/svn/trunk@15 c76b2324-5f53-0410-85ac-b1078a54aeeb
* Try 2 on robustness adding. /  / git-svn-id: http://django-avatar.googlecode.com/svn/trunk@14 c76b2324-5f53-0410-85ac-b1078a54aeeb
* Made falling back more robust. /  / git-svn-id: http://django-avatar.googlecode.com/svn/trunk@13 c76b2324-5f53-0410-85ac-b1078a54aeeb
* Added exception handling for if the directory already exists. /  / git-svn-id: http://django-avatar.googlecode.com/svn/trunk@12 c76b2324-5f53-0410-85ac-b1078a54aeeb
* Added some robustness to import statements. /  / git-svn-id: http://django-avatar.googlecode.com/svn/trunk@11 c76b2324-5f53-0410-85ac-b1078a54aeeb
* Make sure to make the directories before uploading, too. /  / git-svn-id: http://django-avatar.googlecode.com/svn/trunk@10 c76b2324-5f53-0410-85ac-b1078a54aeeb
* Lazy loading doesn't seem to work correctly. /  / git-svn-id: http://django-avatar.googlecode.com/svn/trunk@9 c76b2324-5f53-0410-85ac-b1078a54aeeb
* Screw it, change the wording to be easier on me and translators, yet not be any worsly-worded. /  / git-svn-id: http://django-avatar.googlecode.com/svn/trunk@8 c76b2324-5f53-0410-85ac-b1078a54aeeb
* This isn't Perl /  / git-svn-id: http://django-avatar.googlecode.com/svn/trunk@7 c76b2324-5f53-0410-85ac-b1078a54aeeb
* Fixed bozo error and prettify formatting a bit. /  / git-svn-id: http://django-avatar.googlecode.com/svn/trunk@6 c76b2324-5f53-0410-85ac-b1078a54aeeb
* Added message creation for creation and deletion of avatars. /  / git-svn-id: http://django-avatar.googlecode.com/svn/trunk@5 c76b2324-5f53-0410-85ac-b1078a54aeeb
* Switched the management command to use get_or_create, so that it can create the required Avatar instances for User objects on a new installation. /  / git-svn-id: http://django-avatar.googlecode.com/svn/trunk@4 c76b2324-5f53-0410-85ac-b1078a54aeeb
* Made sure that it really falls back to the specified default. /  / git-svn-id: http://django-avatar.googlecode.com/svn/trunk@3 c76b2324-5f53-0410-85ac-b1078a54aeeb
* Initial version. /  / git-svn-id: http://django-avatar.googlecode.com/svn/trunk@2 c76b2324-5f53-0410-85ac-b1078a54aeeb
* Initial directory structure. /  / git-svn-id: http://django-avatar.googlecode.com/svn/trunk@1 c76b2324-5f53-0410-85ac-b1078a54aeeb
