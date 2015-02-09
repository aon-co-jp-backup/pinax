---
layout: post
title: "django-haystack 1.1.0 Release Notes"
date: 2010-11-23 08:06:40
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-haystack/django-haystack-1.1.0.tar.gz>

This release includes the following:

* Bumped version to v1.1!
* The ``build_solr_schema`` command can now write directly to a file. Also includes tests for the new overrides.
* Haystack's reserved field names are now configurable.
* BACKWARD-INCOMPATIBLE: ``auto_query`` has changed so that only double quotes cause exact match searches. Thanks to craigds for the report!
* Added docs on handling content-type specific output in results.
* Added tests for ``content_type``.
* Added docs on boosting.
* Updated the ``searchfield_api`` docs.
* ``template_name`` can be a list of templates passed to ``loader.select_template``. Thanks to zifot for the suggestion.
* Moved handle_facet_parameters call into FacetField's __init__.
* Updated the pysolr dependency docs & added a debugging note about boost support.
* Starting the beta.
* Fixed a bug with ``FacetedSearchForm`` where ``cleaned_data`` may not exist. Thanks to imageinary for the report!
* Added the ability to build epub versions of the docs.
* Clarified that the current supported version of Whoosh is the 1.1.1+ series. Thanks to glesica for the report & original patch!
* The SearchAdmin now correctly uses SEARCH_VAR instead of assuming things.
* Added the ability to "weight" individual fields to adjust their relevance.
* Fixed facet fieldname lookups to use the proper fieldname.
* Removed unneeded imports from the Solr backend.
* Further revamping of faceting. Each field type now has a faceted variant that's created either with ``faceted=True`` or manual initialization. /  / This should also make user-created field types possible, as many of the gross ``isinstance`` checks were removed.
* Fixes SearchQuerySet not pickleable. Patch by oyiptong, tests by toastdriven.
* Added the ability to remove objects from the index that are no longer in the database to the ``update_index`` management command.
* Added a ``range`` filter type. Thanks to davisp & lukesneeringer for the suggestion! /  / Note that integer ranges are broken on the current Whoosh (1.1.1). However, date & character ranges seem to work fine.
* Consistency.
* Ensured that multiple calls to ``count`` don't result in multiple queries. Thanks to Nagyman and others for the report!
* Ensure that when fetching the length of a result set that the whole index isn't consumed (especially on Whoosh & Xapian).
* Really fixed dict ordering bugs in SearchSite.
* Changed how you query for facets and how how they are presented in the facet counts.  Allows customization of facet field names in indexes. /  / Lightly backward-incompatible (git only).
