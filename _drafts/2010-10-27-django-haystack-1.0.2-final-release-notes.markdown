---
layout: post
title: "django-haystack 1.0.2-final Release Notes"
date: 2010-10-27 02:51:29
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-haystack/django-haystack-1.0.2-final.tar.gz>

This release includes the following:

* Made it easier to override ``SearchView/SearchForm`` behavior when no query is present. /  / No longer do you need to override both ``SearchForm`` & ``SearchView`` if you want to return all results. Use the built-in ``SearchView``, provide your own custom ``SearchForm`` subclass & override the ``no_query_found`` method per the docstring.
* Don't assume that any pk castable to an integer should be an integer.
* Fetching a list of all fields now produces correct results regardless of dict-ordering. Thanks to carljm & veselosky for the report!
* Added notes about what is needed to make schema-building independent of dict-ordering.
* Sorted model order matters.
* Prevent Whoosh from erroring if the ``end_offset`` is less than or equal to 0. Thanks to zifot for the report!
* Removed insecure use of ``eval`` from the Whoosh backend. Thanks to SmileyChris for pointing this out.
* Disallow ``indexed=False`` on ``FacetFields``. Thanks to jefftriplett for the report!
* Added ``FacetField`` & changed the way facets are processed. /  / Facet data is no longer quietly duplicated just before it goes into the index. Instead, full fields are created (with all the standard data & methods) to contain the faceted information. /  / This change is backward-compatible, but allows for better extension, not requiring data duplication into an unfaceted field and a little less magic.
* EmptyQuerySet.facet_counts() won't hit the backend /  / This avoids an unnecessary extra backend query displaying the default / faceted search form.
* TextMate fail.
* Changed ``__name__`` to an attribute on ``SearchView`` to work with decorators. Thanks to trybik for the report!
* Changed some wording on the tutorial to indicate where the data template should go. Thanks for the suggestion Davepar!
* Merge branch 'whoosh-1.1'
* Final cleanup before merging Whoosh 1.1 branch!
* Mistakenly committed this change. This bug is not fixed.
* Better handling of attempts at loading backends when the various supporting libraries aren't installed. Thanks to traviscline for the report.
* Fixed random test failures from not running the Solr tests in awhile.
* Changed mlt test to use a set comparison to eliminate failures due to ordering differences.
* Sped up Solr backend tests by moving away from RealTimeSearchIndex since it was adding objects to Solr when loading fixtures.
* Final Whoosh 1.1.1 fixes. Waiting for an official release of Whoosh & hand testing, then this ought to be merge-able.
* Upgraded the Whoosh backend to 1.1. Still one remaining test failure and two errors. Waiting on mchaput's thoughts/patches.
* Automatically add ``suggestion`` to the context if ``HAYSTACK_INCLUDE_SPELLING`` is set. Thanks to notanumber for the suggestion!
* Added apollo13 to AUTHORS for the ``SearchForm.__init__`` cleanup.
* use kwargs.pop instead of try/except
* Added Rob to AUTHORS for the admin cleanup.
* Fixed selection_note text by adding missing zero
* Fixed full_result_count in admin search results
* Fixed admin actions in admin search results
* Added DevCheatSheet to "Who Uses".
* Added Christchurch Art Gallery to "Who Uses".
* Forgot to include ghostrocket as submitting a patch on the previous commit.
* Fixed a serious bug in the ``simple`` backend that would flip the object instance and class.
* Updated Whoosh to 0.3.18.
* Updated NASA's use of Haystack in "Who Uses".
* Changed how ``ModelSearchIndex`` introspects to accurately use ``IntegerField`` instead of ``FloatField`` as it was using.
* Added CongresoVisible to Who Uses.
* Added a test to verify a previous change to the ``simple`` backend.
* Fixed the new admin bits to not explode on Django 1.1.
* Added ``SearchModelAdmin``, which enables Haystack-based search within the admin.
* Fixed a bug when not specifying a ``limit`` when using the ``more_like_this`` template tag. Thanks to symroe for the original patch.
* Fixed the error messages that occur when looking up attributes on a model. Thanks to acdha for the patch.
* Added pagination to the example search template in the docs so it's clear that it is supported.
* Fixed copy-paste foul in ``Installing Search Engines`` docs.
* Fixed the ``simple`` backend to return ``SearchResult`` instances, not just bare model instances. Thanks to Agos for the report.
* Fixed the ``clear_index`` management command to respect ``--verbosity``. Thanks to kylemacfarlane for the report.
* Altered the ``simple`` backend to only search textual fields. This makes the backend work consistently across all databases and is likely the desired behavior anyhow. Thanks to kylemacfarlane for the report.
* Fixed a bug in the ``Highlighter`` which would double-highlight HTML tags. Thanks to EmilStenstrom for the original patch.
* Updated management command docs to mention all options that are accepted.
* Altered the Whoosh backend to correctly clear the index when using the ``RAMStorage`` backend. Thanks to kylemacfarlane for the initial patch.
* Changed ``SearchView`` to allow more control over how many results are shown per page. Thanks to simonw for the suggestion.
* Ignore ``.pyo`` files when listing out the backend options. Thanks to kylemacfarlane for the report.
* Added CustomMade to Who Uses.
* Moved a backend import to allow changing the backend Haystack uses on the fly. /  / Useful for testing.
* Added more debugging information to the docs.
* Added DeliverGood.org to the "Who Uses" docs.
* Added an settings override on ``HAYSTACK_LIMIT_TO_REGISTERED_MODELS`` as a possible performance optimization.
* Added the ability to pickle ``SearchResult`` objects. Thanks to dedsm for the original patch.
* Added docs and fixed tests on the backend loading portions. Thanks to kylemacfarlane for the report.
* Fixed bug with ``build_solr_schema`` where ``stored=False`` would be ignored. Thanks to johnthedebs for the report.
* Added debugging notes for Solr. Thanks to smccully for reporting this.
* Fixed several errors in the ``simple`` backend. Thanks to notanumber for the original patch.
* Documentation fixes for Xapian. Thanks to notanumber for the edits!
* Fixed a typo in the tutorial. Thanks to cmbeelby for pointing this out.
* Fixed an error in the tutorial. Thanks to bencc for pointing this out.
* Added a warning to the docs that ``SearchQuerySet.raw_search`` does not chain. Thanks to jacobstr for the report.
* Fixed an error in the documentation on providing fields for faceting. Thanks to ghostmob for the report.
* Fixed a bug where a field that's both nullable & faceted would error if no data was provided. Thanks to LarryEitel for the report.
* Fixed a regression where the built-in Haystack fields would no longer facet correctly. Thanks to traviscline for the report.
* Fixed last code snippet on the ``SearchIndex.prepare_FOO`` docs. Thanks to sk1p for pointing that out.
* Fixed a bug where the schema could be built improperly if similar fieldnames had different options.
* Added to existing tests to ensure that multiple faceted fields are included in the index.
* Finally added a README.
* Added a note about versions of the docs.
* Go back to the default Sphinx theme. The custom Haystack theme is too much work and too little benefit.
* Added a note in the tutorial about building the schema when using Solr. Thanks to trey0 for the report!
* Fixed a bug where using ``SearchQuerySet.models()`` on an unregistered model would be silently ignored. /  / It is still silently ignored, but now emits a warning informing the user of why they may receive more results back than they expect.
* Added notes about the ``simple`` backend in the docs. Thanks to notanumber for catching the omission.
* Removed erroneous old docs about Lucene support, which never landed.
* Merge branch 'master' of github.com:toastdriven/django-haystack
* Fixed a bug related to Unicode data in conjunction with the ``dummy`` backend. Thanks to kylemacfarlane for the report!
* Added Forkinit to Who Uses.
* Added Rampframe to Who Uses.
* Fixed typo in the tutorial. Thanks fxdgear for pointing that out!
* Added other apps documentation for Haystack-related apps.
* Unified the way ``DEFAULT_OPERATOR`` is setup.
* You can now override ``ITERATOR_LOAD_PER_QUERY`` with a setting if you're consuming big chunks of a ``SearchQuerySet``. Thanks to kylemacfarlane for the report.
* Moved the preparation of faceting data to a ``SearchIndex.full_prepare()`` method for easier overriding. Thanks to xav for the suggestion!
* The ``more_like_this`` tag now silently fails if things go south. Thanks to piquadrat for the patch!
* Added a fleshed out ``simple_backend`` for basic usage + testing.
* ``SearchView.build_form()`` now accepts a dict to pass along to the form. Thanks to traviscline for the patch!
* Fixed the ``setup.py`` to include ``haystack.utils`` and added to the ``MANIFEST.in``. Thanks to jezdez for the patch!
* Fixed date faceting in Solr. /  / No more OOMs and very fast over large data sets.
* Added the ``search_view_factory`` function for thread-safe use of ``SearchView``.
* Added more to the docs about the ``SearchQuerySet.narrow()`` method to describe when/why to use it.
* Fixed Whoosh tests. /  / Somewhere, a reference to the old index was hanging around causing incorrect failures.
* The Whoosh backed now uses the ``AsyncWriter``, which ought to provide better performance. Requires Whoosh 0.3.15 or greater.
* Added a way to pull the correct fieldname, regardless if it's been overridden or not.
* Added docs about adding new fields.
* Removed a painful ``isinstance`` check which should make non-standard usages easier.
* Updated docs regarding reserved field names in Haystack.
* Pushed some of the new faceting bits down in the implementation.
* Removed unnecessary fields from the Solr schema template.
* Revamped how faceting is done within Haystack to make it easier to work with.
* Add more sites to Who Uses.
* Fixed a bug in ``ModelSearchIndex`` where the ``index_fieldname`` would not get set. Also added a way to override it in a general fashion. Thanks to traviscline for the patch!
* Backend API standardization. Thanks to batiste for the report!
* Removed a method that was supposed to have been removed before 1.0. Oops.
* Added the ability to override field names within the index. Thanks to traviscline for the suggestion and original patch!
* Corrected the AUTHORS because slai actually provided the patch. Sorry about that.
* Refined the internals of ``ModelSearchIndex`` to be a little more flexible. Thanks to traviscline for the patch!
* The Whoosh backend now supports ``RamStorage`` for use with testing or other non-permanent indexes.
* Fixed a bug in the ``Highlighter`` involving repetition and regular expressions. Thanks to alanzoppa for the original patch!
* Fixed a bug in the Whoosh backend when a ``MultiValueField`` is empty. Thanks to alanwj for the original patch!
* All dynamic imports now use ``importlib``. Thanks to bfirsh for the original patch mentioning this. /  / A backported version of ``importlib`` is included for compatibility with Django 1.0.
* Altered ``EmptySearchQuerySet`` so it's usable from templates. Thanks to bfirsh for the patch!
* Added tests to ensure a Whoosh regression is no longer present.
* Fixed a bug in Whoosh where using just ``.models()`` would create an invalid query. Thanks to ricobl for the original patch.
* Forms with initial data now display it when used with SearchView. Thanks to osirius for the original patch.
* App order is now consistent with INSTALLED_APPS when running ``update_index``.
* Updated docs to reflect the recommended way to do imports in when defining ``SearchIndex`` classes. /  / This is not my preferred style but reduces the import errors some people experience.
* Fixed omission of Xapian in the settings docs. Thanks to flebel for pointing this out.
* Little bits of cleanup related to testing.
* Fixed an error in the docs related to pre-rendering data.
* Added Pegasus News to Who Uses.
* Corrected an import in forms for consistency. Thanks to bkonkle for pointing this out.
* Fixed bug where passing a customized ``site`` would not make it down through the whole stack. Thanks to Peter Bengtsson for the report and original patch.
* Bumped copyright years.
* Changed Whoosh backend so most imports will raise the correct exception. Thanks to shabda for the suggestion.
* Refactored Solr's tests to minimize reindexes. Runs ~50% faster.
* Fixed a couple potential circular imports.
* The same field can now have multiple query facets. Thanks to bfirsh for the original patch.
* Added schema for testing Solr.
* Fixed a string interpolation bug when adding an invalid data facet. Thanks to simonw for the original patch.
* Fixed the default highlighter to give slightly better results, especially with short strings. Thanks to RobertGawron for the original patch.
* Changed the ``rebuild_index`` command so it can take all options that can be passed to either ``clear_index`` or ``update_index``. Thanks to brosner for suggesting this.
* Added ``--noinput`` flag to ``clear_index``. Thanks to aljosa for the suggestion.
* Updated the example in the template to be a little more real-world and user friendly. Thanks to j0hnsmith for pointing this out.
* Fixed a bug with the Whoosh backend where scores weren't getting populated correctly. Thanks to horribtastic for the report.
* Changed ``EmptySearchQuerySet`` so it returns an empty list when slicing instead of mistakenly running queries. Thanks to askfor for reporting this bug.
* Switched ``SearchView`` & ``FacetedSearchView`` to use ``EmptySearchQuerySet`` (instead of a regular list) when there are no results. Thanks to acdha for the original patch.
* Added RedditGifts to "Who Uses".
* Added Winding Road to "Who Uses".
* Added ryszard's full name to AUTHORS.
* Added initialization bits to part of the Solr test suite. Thanks to notanumber for pointing this out.
* Started the 1.1-alpha work. Apologies for not doing this sooner.
* Added an advanced setting for disabling Haystack's initialization in the event of a conflict with other apps.
* Altered ``SearchForm`` to use ``.is_valid()`` instead of ``.clean()``, which is a more idiomatic/correct usage. Thanks to askfor for the suggestion.
