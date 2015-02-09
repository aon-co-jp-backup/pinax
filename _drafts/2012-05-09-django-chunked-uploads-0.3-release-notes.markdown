---
layout: post
title: "django-chunked-uploads 0.3 Release Notes"
date: 2012-05-09 04:33:46
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-chunked-uploads/django-chunked-uploads-0.3.tar.gz>

This release includes the following:

* 0.3
* Rewrite stitching method
* Code formatting
* Update string representations of Upload and Chunk
* Increase size of upload file (for longer filenames)
* Add md5 field
* Remove hard coded MEDIA_ROOT
* Completion should be a separate, explicit call that clears the session
* Call a view a view, not a Mixin
