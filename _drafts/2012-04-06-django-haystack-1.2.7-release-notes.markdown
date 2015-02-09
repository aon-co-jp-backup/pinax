---
layout: post
title: "django-haystack 1.2.7 Release Notes"
date: 2012-04-06 09:38:37
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-haystack/django-haystack-1.2.7.tar.gz>

This release includes the following:

* Removed code leftover from v1.X. Thanks to kossovics for the report!
* Fixed a raise condition when using the simple backend (e.g. in tests) and changing the DEBUG setting dynamically (e.g. in integration tests).
* All backends let individual documents fail, rather than failing whole chunks. Forward port of acdha's work on 1.2.X.
* Added ikks to AUTHORS.
* Fixed ``model_choices`` to use ``smart_unicode``.
* +localwiki.org
* Added Pix Populi to "Who Uses".
* Added contribution guidelines.
* Updated the docs to reflect the supported version of Django. Thanks to catalanojuan for the original patch!
* Fix PYTHONPATH Export and add Elasticsearch example
* Updated the Whoosh URL. Thanks to cbess for the original patch!
* Reset database connections on each process on update_index when using --workers
* Moved the ``build_queryset`` method to ``SearchIndex``. /  / This method is used to build the queryset for indexing operations. It is copied / from the build_queryset function that lived in the update_index management / command. /  / Making this change allows developers to modify the queryset used for indexing / even when a date filter is necessary. See `tests/core/indexes.py` for tests.
* Fixed a bug where ``Indexable`` could be mistakenly recognized as a discoverable class. Thanks to twoolie for the original patch!
* Fixed a bug with query construction. Thanks to dstufft for the report! /  / This goes back to erroring on the side of too many parens, where there weren't enough before. The engines will no-op them when they're not important.
* Fixed a bug where South would cause Haystack to setup too soon. Thanks to adamfast for the report!
* Added Crate.io to "Who Uses"!
* Fixed a raise condition when using the simple backend (e.g. in tests) and changing the DEBUG setting dynamically (e.g. in integration tests).
* Fixed a small typo in spatial docs.
* Logging: avoid forcing string interpolation
* Fixed docs on using a template for Solr schema.
* Add note to 'Installing Search Engines' doc explaining how to override the template used by 'build_solr_schema'
* Better handling of ``.models``. Thanks to zbyte64 for the report & HonzaKral for the original patch!
* Added Honza to AUTHORS.
* Handle sorting for ElasticSearch better.
* Update docs/backend_support.rst
* Fixed a bug where it's possible to erroneously try to get spelling suggestions. Thanks to bigjust for the report!
* The ``dateutil`` requirement is now optional. Thanks to arthurnn for the report.
* Fixed docs on Solr spelling suggestion until the new Suggester support can be added. Thanks to zw0rk & many others for the report!
* Bumped to beta. /  / We're not there yet, but we're getting close.
* Added saved-search to subproject docs.
* Search index discovery no longer swallows errors with reckless abandon. Thanks to denplis for the report!
* Elasticsearch backend officially supported. /  / All tests passing.
* Back down to 3 on latest pyelasticsearch.
* And then there were 3 (Elasticsearch test failures).
* Solr tests now run faster.
* Improved the tutorial docs. Thanks to denplis for the report!
* Down to 9 failures on Elasticsearch.
* Because the wishlist has changed.
* A few small fixes. Thanks to robhudson for the report!
* Added an experimental Elasticsearch backend. /  / Tests are not yet passing but it works in basic hand-testing. Passing test coverage coming soon.
* Fixed a bug related to the use of ``Exact``.
* Removed accidental indent.
* Ensure that importing fields without the GeoDjango kit doesn't cause an error. Thanks to dimamoroz for the report!
* Added the ability to reload a connection.
* Fixed ``rebuild_index`` to properly have all options available.
* Fixed a bug in pagination. Thanks to sgoll for the report!
* Added an example to the docs on what to put in ``INSTALLED_APPS``. Thanks to Dan Krol for the suggestion.
* Changed imports so the geospatial modules are only imported as needed.
* Better excluded index detection.
* Fixed a couple of small typos.
* Made sure the toolbar templates are included in the source distribution.
* Fixed a few documentation issues.
* Moved my contribution for the geospatial backend to a attribution of Gidsy which funded my work.
* Small docs fix.
* Added input types, which enables advanced querying support. Thanks to CMGdigital for funding the development!
* Added geospatial search support! /  / I have anxiously waited to add this feature for almost 3 years now. / Support is finally present in more than one backend & I was / generously given some paid time to work on implementing this. /  / Thanks go out to: /  /   * CMGdigital, who paid for ~50% of the development of this feature /     & were awesomely supportive. /   * Jannis Leidel (jezdez), who did the original version of this /     patch & was an excellent sounding board. /   * Adam Fast, for patiently holding my hand through some of the /     geospatial confusions & for helping me verify GeoDjango /     functionality. /   * Justin Bronn, for the great work he originally did on /     GeoDjango, which served as a point of reference/inspiration /     on the API. /  / And thanks to all others who have submitted a variety of / patches/pull requests/interest throughout the years trying to get / this feature in place.
* Added .values() / .values_list() methods, for fetching less data. Thanks to acdha for the original implementation!
* Reduced the number of queries Haystack has to perform in many cases (pagination/facet_counts/spelling_suggestions). Thanks to acdha for the improvements!
* Spruced up the layout on the new DjDT panel.
* Fixed compatibility with Django pre-1.4 trunk. / * The MAX_SHOW_ALL_ALLOWED variable is no longer available, and hence causes an ImportError with Django versions higher 1.3. / * The "list_max_show_all" attribute on the ChangeList object is used instead. / * This patch maintains compatibility with Django 1.3 and lower by trying to import the MAX_SHOW_ALL_ALLOWED variable first.
* Updated ``setup.py`` for the new panel bits.
* Added a basic DjDT panel for Haystack. Thanks to robhudson for planting the seed that Haystack should bundle this!
* Added the ability to specify apps or individual models to ``update_index``. Thanks to CMGdigital for funding this development!
* Added ``--start/--end`` flags to ``update_index`` to allow finer-grained control over date ranges. Thanks to CMGdigital for funding this development!
