---
layout: post
title: "django-bitly 0.5 Release Notes"
date: 2010-07-13 17:23:06
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-bitly/django-bitly-0.5.tar.gz>

This release includes the following:

* Added tag 0.5 for changeset 1e0ca5f70dd2
* upped version number
* merged remote changes
* modified license
* Use simplejson from django.utils
* Added author email to setup.py
* added LICENSE.txt
* merged changes from production branch to fix url matching issue
* fixed issue with url matching failing when it shouldn't
* Added tag 0.4 for changeset 93ec187138cd
* upped version number to 0.4
* Merged abstractbase branch to add in StringHolder model and modified bitlify manager method to allow creation of Bittle objects with nothing other than a string.
* fixed bad syntax for get_or_create /  / --HG-- / branch : abstractbase
* added __unicode__ to StringHolder /  / --HG-- / branch : abstractbase
* Added StringHolder helper model to avoid need for model inheritance. Model simply defines a URL field to hold the URL and a get_absolute_url() method so that a Bittle can be created for it. This allows us to create Bittles with nothing other than a URL in a string. The bitlify() manager method will check if it's being passed a string and, if it is, will automatically create a StringHolder object with it. /  / --HG-- / branch : abstractbase
* start branch for converting Bittle to abstract base class with several sub-classes /  / --HG-- / branch : abstractbase
* removed debug print statements
* debug stuff
* added more helpful error message when object has no get_absolute_url
* added more helpful error message when object has no get_absolute_url
* Added tag 0.3.1 for changeset 8859b787b6c9
* Removed tag 0.3.1
* upped version number to 0.3.1
* Added tag 0.3.1 for changeset 75ccb3e02c29
* updated setup.py to reflect new requirement for Django 1.1+
* Version 0.3, compatible with Django 1.1
* upped version number to 0.3 for Django 1.1 compatibility
* Version 0.2, last release with guaranteed compatibility with Django 1.0.2
* changes for Django 1.1
* added new template filter for displaying a Google Charts pie chart of referrers
* added template tags to retrieve clicks and referrers for an object with a corresponding Bittle, modified example project to demonstrate use /  / --HG-- / rename : example_project/templates/django_bitly/bittle_detail.html => example_project/templates/testapp/testmodel_detail.html / rename : example_project/templates/django_bitly/bittle_list.html => example_project/templates/testapp/testmodel_list.html
* added some very basic support for Bit.ly stats, accessed through new properties on the Bittle model, and cached as a json string in a new editable=False field
* added download_url to setup.py
* Added tag 0.1 for changeset d9e89796c54e
* added template filter that returns bit.ly link for passed object or, failing that, the get_absolute_url. if object has no get_absolute_url it fails silently
* added silent failing to template tag if no get_absolute_url /  / --HG-- / branch : templatetags
* removed unnecessary arg from template filter /  / --HG-- / branch : templatetags
* added bitlify template filter /  / --HG-- / branch : templatetags
* added timestamps to Bittle model, also added basic handling of multiple Bittles per object (will need to be overhauled)
* Removed tag 0.1
* Added tag 0.1 for changeset 4be86439b6f4
* set version to 0.1, ready for initial deployment
* created Bittle model, and custom manager to create Bittle objects for any other object with a get_absolute_url
* added setup.py
* initial commit
