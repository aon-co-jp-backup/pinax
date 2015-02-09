---
layout: post
title: "django-pusher 0.1 Release Notes"
date: 2011-11-22 23:58:55
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-pusher/django-pusher-0.1.tar.gz>

This release includes the following:

* add tempaltetags to packages
* add a basic bit of documentation
* fix package description
* remove the site specific channel key from the channel name
* fix a bug that was causing the if statement to happen at the wrong times
* added a context processor for PUSHER_KEY and a tag to build a channel name
* added urls and view for pusher_auth
* added a method that acts as the original pusher __getitem__. This is needed for authenticate
* added a method to Pusher that will take a request/channel and uses the callback to return True/False for allowing connection
* fix a bug + enable future use of callbacks
* moved the api around a little bit
* small bug fix
* added packaging details
* support for namespaced but not exactly named channels
* allow using Pusher without settings.py settings configured
* instiate a default pusher object that uses the site settings
* added basic pusher api that supports a registry
* initial commit
