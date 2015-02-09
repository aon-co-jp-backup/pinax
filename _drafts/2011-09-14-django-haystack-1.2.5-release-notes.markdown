---
layout: post
title: "django-haystack 1.2.5 Release Notes"
date: 2011-09-14 21:13:25
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-haystack/django-haystack-1.2.5.tar.gz>

This release includes the following:

* Fixed a bug with index inheritance. /      / Fields would seem to not obey the MRO while method did. Thanks to ironfroggy for the report!
* Fixed a long-time bug where the Whoosh backend didn't have a ``log`` attribute.
* Fixed a bug with Whoosh's edge n-gram support to be consistent with the implementation in the other engines.
* Added celery-haystack to Other Apps.
* Changed ``auto_query`` so it can be run on other, non-``content`` fields.
* Removed extra loops through the field list for a slight performance gain.
* Moved ``EXCLUDED_INDEXES`` to a per-backend setting.
* BACKWARD-INCOMPATIBLE: The default filter is now ``__contains`` (in place of ``__exact``). /  / If you were relying on this behavior before, simply add ``__exact`` to the fieldname.
* BACKWARD-INCOMPATIBLE: All "concrete" ``SearchIndex`` classes must now mixin ``indexes.Indexable`` as well in order to be included in the index.
* Added tox to the mix.
* Allow for less configuration. Thanks to jeromer & cyberdelia for the reports!
* Fixed up the management commands to show the right alias & use the default better. Thanks to jeromer for the report!
* Fixed a bug where signals wouldn't get setup properly, especially on ``RealTimeSearchIndex``. Thanks to byoungb for the report!
* Fixed formatting in the tutorial.
* Removed outdated warning about padding numeric fields. Thanks to mchaput for pointing this out!
* Added a silent failure option to prevent Haystack from suppressing some failures. /  / This option defaults to ``True`` for compatibility & to prevent cases where lost connections can break reindexes/searches.
* Fixed the simple backend to not throw an exception when handed an ``SQ``. Thanks to diegobz for the report!
* Whoosh now supports More Like This! Requires Whoosh 1.8.4.
