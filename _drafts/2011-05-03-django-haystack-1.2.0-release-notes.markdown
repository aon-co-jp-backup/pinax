---
layout: post
title: "django-haystack 1.2.0 Release Notes"
date: 2011-05-03 22:35:42
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-haystack/django-haystack-1.2.0.tar.gz>

This release includes the following:

* v1.2.0!
* Added ``request`` to the ``FacetedSearchView`` context. Thanks to dannercustommade for the report!
* Fixed the docs on enabling spelling suggestion support in Solr.
* Fixed a bug so that ``ValuesListQuerySet`` now works with the ``__in`` filter. Thanks to jcdyer for the report!
* Added the new ``SearchIndex.read_queryset`` bits.
* Changed ``update_index`` so that it warns you if your ``SearchIndex.get_queryset`` returns an unusable object.
* Removed Python 2.3 compat code & bumped requirements for the impending release.
* Added treyhunner to AUTHORS.
* Improved the way selected_facets are handled. /  / * ``selected_facets`` may be provided multiple times. / * Facet values are quoted to avoid backend confusion (i.e. `author:Joe Blow` is seen by Solr as `author:Joe AND Blow` rather than the expected `author:"Joe Blow"`)
* Add test for Whoosh field boost
* Enable field boosting with Whoosh backend
* Fixed the Solr & Whoosh backends to use the correct ``site`` when processing results. Thanks to Madan Thangavelu for the original patch!
* Added lukeman to AUTHORS.
* Updating Solr download and installation instructions to reference version 1.4.1 as 1.3.x is no longer available. Fixes #341.
* Revert "Shifted ``handle_registrations`` into ``models.py``." /  / This seems to be breaking for people, despite working here & passing tests. Back to the drawing board... /  / This reverts commit 106758f88a9bc5ab7e505be62d385d876fbc52fe.
* Shifted ``handle_registrations`` into ``models.py``. /  / For historical reasons, it was (wrongly) kept & run in ``__init__.py``. This should help fix many people's issues with it running too soon.
* Pulled out ``EmptyResults`` for testing elsewhere.
* Fixed a bug where boolean filtering wouldn't work properly on Whoosh. Thanks to alexrobbins for pointing it out!
* Added link to 1.1 version of the docs.
* Whoosh 1.8.1 compatibility.
* Added TodasLasRecetas to "Who Uses". Thanks Javier!
* Added a new method to ``SearchQuerySet`` to allow you to specify a custom ``result_class`` to use in place of ``SearchResult``. Thanks to aaronvanderlip for getting me thinking about this!
* Added better autocomplete support to Haystack.
* Changed ``SearchForm`` to be more permissive of missing form data, especially when the form is unbound. Thanks to cleifer for pointing this out!
* Ensured that the primary key of the result is a string. Thanks to gremmie for pointing this out!
* Fixed a typo in the tutorial. Thanks to JavierLopezMunoz for pointing this out!
* Added appropriate warnings about ``HAYSTACK_<ENGINE>_PATH`` settings in the docs.
* Added some checks for badly-behaved backends.
* Ensure ``use_template`` can't be used with ``MultiValueField``.
* Added n-gram fields for auto-complete style searching.
* Added ``django-celery-haystack`` to the subapp docs.
* Fixed the the faceting docs to correctly link to narrowed facets. Thanks to daveumr for pointing that out!
* Updated docs to reflect the ``form_kwargs`` that can be used for customization.
* Whoosh backend now explicitly closes searchers in an attempt to use fewer file handles.
* Changed fields so that ``boost`` is now the parameter of choice over ``weight`` (though ``weight`` has been retained for backward compatibility). Thanks to many people for the report!
* Bumped revision.
