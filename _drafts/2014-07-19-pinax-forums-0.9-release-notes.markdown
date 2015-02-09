---
layout: post
title: "pinax-forums 0.9 Release Notes"
date: 2014-07-19 19:55:56
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/p/pinax-forums/pinax-forums-0.9.tar.gz>

This release includes the following:

* Some things missed in the rename
* Fix some badge typos
* Rename agora to pinax-forums and move to Pinax organization /  / agora was developed a while ago for Eldarion clients who permitted us / open sourcing it. We open sourced it under the name agora as Eldarion / open source but from the start it was considered part of Pinax. /  / Since we have yet to release a package and are preparing to do so, it / made sense to relocate the package under the Pinax organization and / rename it to something so it’s clearly a Pinax app.
* Add some tests
* Add coverage settings
* No need to support earlier versions for Django at this point
* Add test infrastructure
* Fix lint issues
* Clean up some style
* Upgrade appconf requirement
* Update README.rst
* Create .travis.yml
* changed link to Pinax Forums
* back to RST
* missing newline
* updated README
* Clean up style
* Remove url defaults import
* Increment copyright year
* updated LICENSE year
* Fix a minor undefined name bug
* Remove unused signal
* Fix bug in calls to @receiver
* Use AppConf for app-level configuration
* Conform to style guide / PEP8
* Put receivers in their own module
* Use timezone.now instead of datetime.datetime.now
* Use system json
* Add templatetags to package
* Fix ordering
* Update agora/views.py
* added forum closed and some other tweaks to permissions
* fixed call to has_perm
* tweaked error message on no reply permission
* added permission check with reply form on thread
* added permissions
* added blank=True to ForumThread.closed
* added thread closed
* changed quick reply to use a django form
* added sticky to forum threads
* added AGORA_EDIT_TIMEOUT setting
* fixed default_text escaping
* added custom markup support through AGORA_PARSER
* implemented proper deletion for threads and replies
* added missing forms.py
* removed duplicate URL
* use django forms
* tweaked view and URL names
* pass in thread and not only the thread ID
* finished fully implementing posts
* fixed spacing
* use on_delete to prevent accidental data deletion
* 0.1.dev16
* need a set here
* 0.1.dev15
* fix for 2.4
* 0.1.dev14
* removed limiting allowing template to deal with it
* various tweaks
* 0.1.dev12
* added onsite subscriptions
* added UserPostCount.calculate
* set _importing attribute while restoring allowing signal handlers to ignore it
* 0.1.dev9
* added Forum export and restoration methods
* tweaks for supporting ThreadSubscription (does not send notifications)
* cleaned up signal registration
* fixed a typo
* 0.1.dev6
* Merge branch 'subscription-tags'
* Adding views and tags for thread subscriptions.
* fixed some bugs with iteration in ForumThreadPostQuerySet and added kind to make it simpler to determine what object it is in template
* support thread and reply editing
* added ForumThread.objects.post to yield all posts including itself; supports decent reverse yielding too
* moved out common elements between ForumThread and ForumReply to ForumPost abstract base class
* fixed MANIFEST.in
* added MANIFEST.in to fix some missing files
* 0.1.dev2
* some fixes to get things working a bit better
* minor clean-ups
* various fixes and name changes
* more view fixes
* various fixes to views
* fixed various issues that came up during testing
* fixed import error and got rid of category pagination for now
* added admin interface for some models (with tweaks to models to make them more usable)
* fixed up fieldname change in view
* fixed up imports and some legacy code
* added initial views and urls
* added missing import
* more consistent field naming
* added setup.py
* added note about need to implement deletion handling
* added a unique_together for ThreadSubscription
* added note about handling unsubscribe
* added note about supporting markup
* added note questioning where to notify subscribers
* switched approach to have content on thread and not make is_first distinction on post, renaming it reply instead
* added note about features to do: sticky threads, closed threads
* added thread subscriptions
* initial models
* initial app skeleton
