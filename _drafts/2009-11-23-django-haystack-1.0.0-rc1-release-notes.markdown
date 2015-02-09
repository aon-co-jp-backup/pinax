---
layout: post
title: "django-haystack 1.0.0-rc1 Release Notes"
date: 2009-11-23 08:18:56
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-haystack/django-haystack-1.0.0-rc1.tar.gz>

This release includes the following:

* Marked Haystack as 1.0.0 release candidate 1.
* Haystack now requires Whoosh 0.3.5.
* Last minute documentation cleanup.
* Added documentation about the management commands that come with Haystack.
* Added docs on the template tags included with Haystack.
* Added docs on highlighting.
* Removed some unneeded legacy code that was causing conflicts when Haystack was used with apps that load all models (such as `django-cms2`, `localemiddleware` or `django-transmeta`).
* Removed old code from the `update_index` command.
* Altered spelling suggestion test to something a little more consistent.
* Added tests for slicing the end of a `RelatedSearchQuerySet`.
* Fixed case where `SearchQuerySet.more_like_this` would fail when using deferred Models. Thanks to Alex Gaynor for the original patch.
* Added default logging bits to prevent "No handlers found" message.
* BACKWARD-INCOMPATIBLE: Renamed `reindex` management command to `update_index`, renamed `clear_search_index` management command to `clear_index` and added a `rebuild_index` command to both clear & reindex.
* BACKWARD-INCOMPATIBLE: `SearchIndex` no longer hooks up `post_save/post_delete` signals for the model it's registered with. /  / If you use `SearchIndex`, you will have to manually cron up a `reindex` (soon to become `update_index`) management command to periodically refresh the data in your index. /  / If you were relying on the old behavior, please use `RealTimeSearchIndex` instead, which does hook up those signals.
* Ensured that, if a `MultiValueField` is marked as `indexed=False` in Whoosh, it ought not to post-process the field.
* Ensured data going into the indexes round-trips properly. Fixed `DateField`/`DateTimeField` handling for all backends and `MultiValueField` handling in Whoosh.
* Added a customizable `highlight` template tag plus an underlying `Highlighter` implementation.
* Added more documentation about using custom `SearchIndex.prepare_FOO` methods.
* With Whoosh 0.3.5+, the number of open files is greatly reduced.
* Corrected example in docs about `RelatedSearchQuerySet`. Thanks to askfor for pointing this out.
* Altered `SearchResult` objects to fail gracefully when the model/object can't be found. Thanks to akrito for the report.
* Fixed a bug where `auto_query` would fail to escape strings that pulled out for exact matching. Thanks to jefftriplett for the report.
* Added Brick Design to Who Uses.
* Updated backend support docs slightly.
* Added the ability to combine `SearchQuerySet`s via `&` or `|`. Thanks to reesefrancis for the suggestion.
* Revised the most of the tutorial.
* Better documented how user-provided data should be sanitized.
* Fleshed out the `SearchField` documentation.
* Fixed formatting on ``SearchField`` documentation.
* Added basic ``SearchField`` documentation. /  / More information about the kwargs and usage will be eventually needed.
* Bumped the `ulimit` so Whoosh tests pass consistently on Mac OS X.
* Fixed the `default` kwarg in `SearchField` (and subclasses) to work properly from a user's perspective.
* BACKWARD-INCOMPATIBLE: Fixed ``raw_search`` to cooperate when paginating/slicing as well as many other conditions. /  / This no longer immediately runs the query, nor pokes at any internals. It also now takes into account other details, such as sorting & faceting.
* Fixed a bug in the Whoosh backend where slicing before doing a hit count could cause strange results when paginating. Thanks to kylemacfarlane for the original patch.
* The Whoosh tests now deal with the same data set as the Solr tests and cover various aspects better.
* Started to pull out the real-time, signal-based updates out of the main `SearchIndex` class. Backward compatible for now.
* Fixed docs to include `utils` documentation.
* Updated instructions for installing `pysolr`. Thanks to sboisen for pointing this out.
* Added acdha to AUTHORS for previous commit.
* Added exception handling to the Solr Backend to silently fail/log when Solr is unavailable. Thanks to acdha for the original patch.
* The `more_like_this` tag is now tested within the suite. Also has lots of cleanup for the other Solr tests.
* On both the Solr & Whoosh backends, don't do an update if there's nothing being updated.
* Moved Haystack's internal fields out of the backends and into `SearchIndex.prepare`. /  / This is both somewhat more DRY as well as a step toward Haystack being useful to non-Django projects.
* Fixed a bug in the `build_schema` where fields that aren't supposed to be indexed are still getting post-procesed by Solr. Thanks to Jonathan Slenders for the report.
* Added HUGE to Who Uses.
* Fixed bug in Whoosh where it would always generate spelling suggestions off the full query even when given a different query string to check against.
* Simplified the SQ object and removed a limitation on kwargs/field names that could be passed in. Thanks to traviscline for the patch.
* Documentation on `should_update` fixed to match the new signature. Thanks to kylemacfarlane for pointing this out.
* Fixed missing words in Best Practices documentation. Thanks to frankwiles for the original patch.
* The `update_object` method now passes along kwargs as needed to the `should_update` method. Thanks to askfor for the suggestion.
* Updated docs about the removal of the Whoosh fork.
* Removed extraneous `BadSearchIndex3` from test suite. Thanks notanumber!
* We actually want `repr`, not `str`.
* Pushed the `model_attr` check lower down into the `SearchField`s and make it occur later, so that exceptions come at a point where Django can better deal with them.
* Fixed attempting to access an invalid `model_attr`. Thanks to notanumber for the original patch.
* Added SQ objects (replacing the QueryFilter object) as the means to generate queries/query fragments. Thanks to traviscline for all the hard work. /  / The SQ object is similar to Django's Q object and allows for arbitrarily complex queries. Only backward incompatible if you were relying on the SearchQuery/QueryFilter APIs.
* Reformatted debugging docs a bit.
* Added debugging information about the Whoosh lock error.
* Brought the TODO up to date.
* Added a warning to the documentation about how `__startswith` may not always provide the expected results. Thanks to codysoyland for pointing this out.
* Added debugging documentation, with more examples coming in the future.
* Added a new `basic_search` view as a both a working example of how to write traditional views and as a thread-safe view, which the class-based ones may/may not be.
* Fixed sample template in the documentation. Thanks to lemonad for pointing this out.
* Updated documentation to include a couple more Sphinx directives. Index is now more useful.
* Made links more obvious in documentation.
* Added an `example_project` demonstrating how a sample project might be setup.
* Fixed `load_backend` to use the argument passed instead of always the `settings.HAYSTACK_SEARCH_ENGINE`. Thanks to newgene for the report.
* Regression where sometimes `narrow_queries` got juggled into a list when it should be a set everywhere. Thanks tcline & ericholscher for the report.
* Updated the Whoosh backend's version requirement to reflect the fully working version of Whoosh.
* With the latest SVN version of Whoosh (r344), `SearchQuerySet()` now works properly in Whoosh.
* Added a `FacetedModelSearchForm`. Thanks to mcroydon for the original patch.
* Added translation capabilities to the `SearchForm` variants. Thanks to hejsan for pointing this out.
* Added AllForLocal to Who Uses.
* The underlying caching has been fixed so it no longer has to fill the entire cache before it to ensure consistency. /  / This results in significantly faster slicing and reduced memory usage. The test suite is more complete and ensures this functionality better. /  / This also removes `load_all_queryset` from the main `SearchQuerySet` implementation. If you were relying on this behavior, you should use `RelatedSearchQuerySet` instead.
* Log search queries with `DEBUG = True` for debugging purposes, similar to what Django does.
* Updated LJ's Who Uses information.
* Added Sunlight Labs & NASA to the Who Uses list.
* Added Eldarion to the Who Uses list.
* When more of the cache is populated, provide a more accurate `len()` of the `SearchQuerySet`. This ought to only affect advanced usages, like excluding previously-registered models or `load_all_queryset`.
* Fixed a bug where `SearchQuerySet`s longer than `REPR_OUTPUT_SIZE` wouldn't include a note about truncation when `__repr__` is called.
* Added the ability to choose which site is used when reindexing. Thanks to SmileyChris for pointing this out and the original patch.
* Fixed the lack of a `__unicode__` method on `SearchResult` objects. Thanks to mint_xian for pointing this out.
* Typo'd the setup.py changes. Thanks to jlilly for catching that.
* Converted all query strings to Unicode for Whoosh. Thanks to simonw108 for pointing this out.
* Added template tags to `setup.py`. Thanks to Bogdan for pointing this out.
* Added two more tests to the Whoosh backend, just to make sure.
* Corrected the way Whoosh handles `order_by`. Thanks to Rowan for pointing this out.
* For the Whoosh backend, ensure the directory is writable by the current user to try to prevent failed writes.
* Added a better label to the main search form field.
* Bringing the Whoosh backend up to version 0.3.0b14. This version of Whoosh has better query parsing, faster indexing and, combined with these changes, should cause fewer disruptions when used in a multiprocess/multithreaded environment.
* Added optional argument to `spelling_suggestion` that lets you provide a different query than the one built by the SearchQuerySet. /  / Useful for passing along a raw user-provided query, especially when there is a lot of post-processing done.
* SearchResults now obey the type of data chosen in their corresponding field in the SearchIndex if present. Thanks to evgenius for the original report.
* Fixed a bug in the Solr backend where submitting an empty string to search returned an ancient and incorrect datastructure. Thanks kapa77 for the report.
* Fixed a bug where the cache would never properly fill due to the number of results returned being lower than the hit count. This could happen when there were results excluded due to being in the index but the model NOT being registered in the `SearchSite`. Thanks akrito and tcline for the report.
* Altered the docs to look more like the main site.
* Added a (short) list of who uses Haystack. Would love to have more on this list.
* Fixed docs on preparing data. Thanks fud.
* Added the `ModelSearchIndex` class for easier `SearchIndex` generation.
* Added a note about using possibly unsafe data with `filter/exclude`. Thanks to ryszard for pointing this out.
* Standardized the API on `date_facet`. Thanks to notanumber for the original patch.
* Moved constructing the schema down to the `SearchBackend` level. This allows more flexibility when creating a schema.
* Fixed a bug where a hyphen provided to `auto_query` could break the query string. Thanks to ddanier for the report.
* BACKWARD INCOMPATIBLE - For consistency, `get_query_set` has been renamed to `get_queryset` on `SearchIndex` classes. /  / A simple search & replace to remove the underscore should be all that is needed.
* Missed two bits while updating the documentation for the Xapian backend.
* Updated documentation to add the Xapian backend information. A big thanks to notatnumber for all his hard work on the Xapian backend.
* Added `EmptySearchQuerySet`. Thanks to askfor for the suggestion!
* Added "Best Practices" documentation.
* Added documentation about the `HAYSTACK_SITECONF` setting.
* Fixed erroneous documentation on Xapian not supporting boost. Thanks notanumber!
* BACKWARD INCOMPATIBLE - The `haystack.autodiscover()` and other site modifications now get their own configuration file and should no longer be placed in the `ROOT_URLCONF`. Thanks to SmileyChris for the original patch and patrys for further feedback.
* Added `verbose_name_plural` to the `SearchResult` object.
* Added a warning about ordering by integers with the Whoosh backend.
* Added a note about ordering and accented characters.
* Updated the `more_like_this` tag to allow for narrowing the models returned by the tag.
* Fixed `null=True` for `IntegerField` and `FloatField`. Thanks to ryszard for the report and original patch.
* Reverted aabdc9d4b98edc4735ed0c8b22aa09796c0a29ab as it would cause mod_wsgi environments to fail in conjunction with the admin on Django 1.1.
* Added the start of a glossary of terminology.
* Various documentation fixes. Thanks to sk1p & notanumber.
* The `haystack.autodiscover()` and other site modifications may now be placed in ANY URLconf, not just the `ROOT_URLCONF`. Thanks to SmileyChris for the original patch.
* Fixed invalid/empty pages in the SearchView. Thanks to joep and SmileyChris for patches.
* Added a note and an exception about consistent fieldnames for the document field across all `SearchIndex` classes. Thanks sk1p_!
* Possible thread-safety fix related to registration handling.
* BACKWARD INCOMPATIBLE - The 'boost' method no longer takes kwargs. This makes boost a little more useful by allowing advanced terms. /  / To migrate code, convert multiple kwargs into separate 'boost' calls, quote what was the key and change the '=' to a ','.
* Updated documentation to match behavioral changes to MLT.
* Fixed a serious bug in MLT on Solr. Internals changed a bit and now things work correctly.
* Removed erroneous 'zip_safe' from setup.py. Thanks ephelon.
* Added `null=True` to fields, allowing you to ignore/skip a field when indexing. Thanks to Kevin for the original patch.
* Fixed a standing test failure. The dummy setup can't do `load_all` due to mocking.
* Added initial `additional_query` to MLT to allow for narrowing results.
* Fixed nasty bug where results would get duplicated due to cached results.
* Altered `ITERATOR_LOAD_PER_QUERY` from 20 to 10.
* Corrected tutorial when dealing with fields that have `use_template=True`.
* Updated documentation to reflect basic Solr setup.
* Fix documentation on grabbing Whoosh and on the 'load_all' parameter for SearchForms.
* Fixed bug where the '__in' filter wouldn't work with phrases or data types other than one-word string/integer.
* Fixed bug so that the 'load_all' option in 'SearchView' now actually does what it says it should. How embarrassing...
* Added ability to specify custom QuerySets for loading records via 'load_all'/'load_all_queryset'.
* Fixed a bug where results from non-registered models could appear in the results.
* BACKWARD INCOMPATIBLE - Changed 'module_name' to 'model_name' throughout Haystack related to SearchResult objects. Only incompatible if you were relying on this attribute.
* Added the ability to fetch additional and stored fields from a SearchResult as well as documentation on the SearchResult itself.
* Added the ability to look through relations in SearchIndexes via '__'.
* Added note about the 'text' fieldname convention.
* Added an 'update_object' and 'remove_object' to the SearchSite objects as a shortcut.
* Recover gracefully from queries Whoosh judges to be invalid.
* Missed test from previous commit.
* Added stemming support to Whoosh.
* Removed the commented version.
* Django 1.0.X compatibility fix for the reindex command.
* Reindexes should now consume a lot less RAM. /  / Evidently, when you run a ton of queries touching virtually everything in your DB, you need to clean out the "logged" queries from the connection. Sad but true.
* Altered `SearchBackend.remove` and `SearchBackend.get_identifier` to accept an object or a string identifier (in the event the object is no longer available). /  / This is useful in an environment where you no longer have the original object on hand and know what it is you wish to delete.
* Added a simple (read: ghetto) way to run the test suite without having to mess with settings.
* Added a setting `HAYSTACK_BATCH_SIZE` to control how many objects are processed at once when running a reindex.
* Fixed import that was issuing a warning.
* Further tests to make sure `unregister` works appropriately as well, just to be paranoid.
* Fixed a bizarre bug where backends may see a different site object than the rest of the application code. THIS REQUIRES SEARCH & REPLACING ALL INSTANCES OF `from haystack.sites import site` TO `from haystack import site`. /  / No changes needed if you've been using `haystack.autodiscover()`.
* Pushed save/delete signal registration down to the SearchIndex level. /  / This should make it easier to alter how individual indexes are setup, allowing you to queue updates, prevent deletions, etc. The internal API changed slightly.
* Created a default 'clean' implementation, as the first three (and soon fourth) backends all use identical code.
* Updated tests to match new 'model_choices'.
* Added timeout support to Solr.
* Capitalize the Models in the model_choices.
* Removed unnecessary import.
* No longer need to watch for DEBUG in the 'haystack_info' command.
* Fixed bug in Whoosh backend when spelling suggestions are disabled.
* Added a "clear_search_index" management command.
* Removed comments as pysolr now supports timeouts and the other comment no longer applies.
* Removed Solr-flavored schema bits. /  / Still need to work out a better way to handle user created fields that don't fit neatly into subclassing one of the core Field types.
* Moved informational messages to a management command to behave better when using dumpdata or wsgi.
* Changed some Solr-specific field names. Requires a reindex.
* Typo'd docstring.
* Removed empty test file from spelling testing.
* Documentation for getting spelling support working on Solr.
* Initial spelling support added.
* Added a 'more_like_this' template tag.
* Removed an unnecessary 'run'. This cause MLT (and potentially 'raw_search') to fail by overwriting the results found.
* Added Whoosh failure. Needs inspecting.
* Finally added views/forms documentation. A touch rough still.
* Fixed a bug in FacetedSearchView where a SearchQuerySet method could be called on an empty list instead.
* More faceting documentation.
* Started faceting documentation.
* Updated docs to finally include details about faceting.
* Empty or one character searches in Whoosh returned the wrong data structure. Thanks for catching this, silviogutierrez!
* Added scoring to Whoosh now that 0.1.20+ support it.
* Fixed a bug in the Solr tests due to recent changes in pysolr.
* Added documentation on the 'narrow' method.
* Added additional keyword arguments on raw_search.
* Added 'narrow' support in Whoosh.
* Fixed Whoosh backend's handling of pre-1900 dates. Thanks JoeGermuska!
* Backed out the Whoosh quoted dates patch. /  / Something still seems amiss in the Whoosh query parser, as ranges and dates together don't seem to get parsed together properly.
* Added a small requirements section to the docs.
* Added notes about enabling the MoreLikeThisHandler within Solr.
* Revised how tests are done so each backend now gets its own test app. /  / All tests pass once again.
* Added 'startswith' filter.
* Fixed the __repr__ method on QueryFilters. Thanks JoeGermuska for the original patch!
* BACKWARDS INCOMPATIBLE - Both the Solr & Whoosh backends now provide native Python types back in SearchResults. /  / This also allows Whoosh to use native types better from the 'SearchQuerySet' API itself. /  / This unfortunately will also require all Whoosh users to reindex, as the way some data (specifically datetimes/dates but applicable to others) is stored in the index.
* SearchIndexes now support inheritance. Thanks smulloni!
* Added FacetedSearchForm to make handling facets easier.
* Heavily refactored the SearchView to take advantage of being a class. /  / It should now be much easier to override bits without having to copy-paste the entire __call__ method, which was more than slightly embarrassing before.
* Fixed Solr backend so that it properly converts native Python types to something Solr can handle. Thanks smulloni for the original patch!
* SearchResults now include a verbose name for display purposes.
* Fixed reverse order_by's when using Whoosh. Thanks matt_c for the original patch.
* Handle Whoosh stopwords behavior when provided a single character query string.
* Lightly refactored tests to only run engines with their own settings.
* Typo'd the tutorial when setting up your own SearchSite. Thanks mcroydon!
* Altered loading statements to only display when DEBUG is True.
* Write to STDERR where appropriate. Thanks zerok for suggesting this change.
* BACKWARD INCOMPATIBLE - Altered the search query param to 'q' instead of 'query'. Thanks simonw for prompting this change.
* Removed the Whoosh patch in favor of better options. Please see the documentation.
* Added Whoosh patch for 0.1.15 to temporarily fix reindexes.
* Altered the reindex command to handle inherited models. Thanks smulloni!
* Removed the no longer needed Whoosh patch. /  / Whoosh users should upgrade to the latest Whoosh (0.1.15) as it fixes the issues that the patch covers as well as others.
* Documented the 'content' shortcut.
* Fixed an incorrect bit of documentation on the default operator setting. Thanks benspaulding!
* Added documentation about Haystack's various settings.
* Corrected an issue with the Whoosh backend that can occur when no indexes are registered. Now provides a better exception.
* Documentation fixes. Thanks benspaulding!
* Fixed Whoosh patch, which should help with the "KeyError" exceptions when searching with models. Thanks Matias Costa!
* Improvements to the setup.py. Thanks jezdez & ask!
* Fixed the .gitignore. Thanks ask!
* FacetedSearchView now inherits from SearchView. Thanks cyberdelia! /  / This will matter much more soon, as SearchView is going to be refactored to be more useful and extensible.
* Documentation fixes.
* Altered the whoosh patch. Should apply cleanly now.
* Better linking to the search engine installation notes.
* Added documentation on setting up the search engines.
* Provide an exception when importing a backend dependency fails. Thanks brosner for the initial patch.
* Yay stupid typos!
* Relicensing under BSD. Thanks matt_c for threatening to use my name in an endorsement of a derived product!
* Fixed a bug in ModelSearchForm. Closes #1. Thanks dotsphinx!
* Added link to pysolr binding.
* Refined documentation on preparing SearchIndex data.
* Changed existing references from 'model_name' to 'module_name'. /  / This was done to be consistent both internally and with Django. Thanks brosner!
* Documentation improvements. Restyled and friendlier intro page.
* Added documentation on preparing data.
* Additions and re-prioritizing the TODO list.
* Added warnings to Whoosh backend in place of silently ignoring unsupported features.
* Corrected Xapian's capabilities. Thanks richardb!
* BACKWARD INCOMPATIBLE - Altered all settings to be prefixed with HAYSTACK_. Thanks Collin!
* Test cleanup from previous commits.
* Changed the DEFAULT_OPERATOR back to 'AND'. Thanks richardb!
* Altered the way registrations get handled.
* Various fixes. Thanks brosner!
* Added new 'should_update' method to documentation.
* Added 'should_update' method to SearchIndexes. /  / This allows you to control, on a per-index basis, what conditions will cause an individual object to reindex. Useful for models that update frequently with changes that don't require indexing.
* Added FAQ docs.
* Alter Whoosh backend to commit regardless. This avoids locking issues that can occur on higher volume sites.
* A more efficient implementation of index clearing in Whoosh.
* Added details about settings needed in settings.py.
* Added setup.py. Thanks cyberdelia for prompting it.
* Reindex management command now can reindex a limited range (like last 24 hours). Thanks traviscline.
* More things to do.
* Documentation formatting fixes.
* Added SearchBackend docs.
* Corrected reST formatting.
* Additional TODO's.
* Initial SearchIndex documentation.
* Formally introduced the TODO.
* Updated backend support list.
* Added initial documentation for SearchSites.
* Changed whoosh backend to fix limiting sets. Need to revisit someday.
* Added patch for Whoosh backend and version notes in documentation.
* Initial Whoosh backend complete. /  / Does not yet support highlighting or scoring.
* Removed some unnecessary dummy code.
* Work on trying to get the default site to load reliably in all cases.
* Trimmed down the urls for tests now that the dummy backend works correctly.
* Dummy now correctly loads the right SearchBackend.
* Removed faceting from the default SearchView.
* Refactored tests so they are no longer within the haystack app. /  / Further benefits include less mocking and haystack's tests no longer contributing overall testing of end-user apps. Documentation included.
* Removed old comment.
* Fixed a potential race condition. Also, since there's no way to tell when everything is ready to go in Django, adding an explicit call to SearchQuerySet's __init__ to force the site to load if it hasn't already.
* More tests on models() support.
* Pulled schema building out into the site to leverage across backends.
* Altered backend loading for consistency with Django and fixed the long-incorrect-for-non-obvious-and-tedious-reasons version number. Still beta but hopefully that changes soon.
* Missed a spot when fixing SearchSites.
* BACKWARD INCOMPATIBLE - Created a class name conflict during the last change (double use of ``SearchIndex``). Renamed original ``SearchIndex`` to ``SearchSite``, which is slightly more correct anyhow. /  / This will only affect you if you've custom built sites (i.e. not used ``autodiscover()``.
* More documentation. Started docs on SearchQuery.
* Further fleshed out SearchQuerySet documentation.
* BACKWARD INCOMPATIBLE (2 of 2) - Altered autodiscover to search for 'search_indexes.py' instead of 'indexes.py' to prevent collisions and be more descriptive.
* BACKWARD INCOMPATIBLE (1 of 2) - The ModelIndex class has been renamed to be SearchIndex to make room for future improvements.
* Fleshed out a portion of the SearchQuerySet documentation.
* SearchQuerySet.auto_query now supports internal quoting for exact matches.
* Fixed semi-serious issue with SearchQuery objects, causing bits to leak from one query to the next when cloning.
* Altered Solr port for testing purposes.
* Now that Solr and core feature set are solid, moved haystack into beta status.
* Added simple capabilities for retrieving facets back.
* Bugfix to make sure model choices don't get loaded until after the IndexSite is populated.
* Initial faceting support complete.
* Query facets tested.
* Bugfix to (field) facets. /  / Using a dict is inappropriate, as the output from Solr / is sorted by count. Now using a two-tuple.
* Backward-incompatible changes to faceting. Date-based faceting is now present.
* Solr implementation of faceting started. Needs more tests.
* Initial faceting support in place. Needs more thought and a Solr implementation.
* Unbreak iterables in queries.
* Bugfixes for Unicode handling and loading deleted models.
* Fixed bug in Solr's run method.
* Various bug fixes.
* Backward-Incompatible: Refactored ModelIndexes to allow greater customization before indexing. See "prepare()" methods.
* Updated "build_solr_schema" command for revised fields.
* Refactored SearchFields. Lightly backwards-incompatible.
* No more duplicates from the "build_solr_schema" management command.
* Removed the kwargs. Explicit is better than implicit.
* Tests for highlighting.
* Added initial highlighting support. Needs tests and perhaps a better implementation.
* Started "build_solr_schema" command. Needs testing with more than one index.
* Argh. ".select_related()" is killing reindexes. Again.
* Stored fields now come back as part of the search result.
* Fixed Solr's SearchQuery.clean to handle reserved words more appropriately.
* Filter types seem solid and have tests.
* App renamed (for namespace/sanity/because it's really different reasons).
* Started trying to support the various filter types. Needs testing and verification.
* Fixed tests in light of the change to "OR".
* Readded "select_related" to reindex command.
* I am a moron.
* "OR" is now the default operator. Also, "auto_query" now handles not'ed keywords.
* "More Like This" now implemented and functioning with Solr backend.
* Removed broken references to __name__.
* Internal documentation fix.
* Solr backend can now clear on a per-model basis.
* Solr backend tests fleshed out. Initial stability of Solr. /  / This needs more work (as does everything) but it seems to be working reliably from my testing (both unit and "real-world"). Onward and upward.
* Massive renaming/refactoring spree. Tests 100% passing again.
* Renamed BaseSearchQuerySet to SearchQuerySet. Now requires instantiation.
* Standardizing syntax.
* Backend support update.
* An attempt to make sure the main IndexSite is always setup, even outside web requests. Also needs improvement.
* Reindexes now work.
* Some painful bits to make things work for now. Needs improvement.
* Support kwargs on the search.
* Move solr backend tests in prep for fully testing the backend.
* Some ContentField/StoredField improvements. /  / StoredFields now have a unique template per field (as they should have from the start) and there's a touch more checking. You can also now override the template name for either type of field.
* Fixed backend loading upon unpickling SearchBackend.
* Tweak internal doc.
* MOAR DOCS.
* Internal documentation and cleanup. Also alters the behavior of SearchQuerySet's "order_by" method slightly, bringing it more in-line with QuerySet's behavior.
* Documentation/license updates.
* Fixed ModelIndexes and created tests for them. 100% tests passing again.
* Started refactoring ModelIndexes. Needs tests (and possibly a little love).
* Implemented Solr's boost, clean, multiple order-by. Fixed Solr's score retrieval (depends on custom pysolr) and exact match syntax.
* Minor changes/cleanup.
* Updated docs and a FIXME.
* SearchView/SearchForm tests passing.
* Changed BaseSearchQuery to accept a SearchBackend instance instead of the class.
* Better dummy implementation, a bugfix to raw_search and SearchView/SearchForm tests.
* Temporarily changed the Solr backend to ignore fields. Pysolr will need a patch and then reenable this.
* Merge branch 'master' of ssh://daniel@mckenzie/home/daniel/djangosearch_refactor into HEAD
* Started SearchView tests and added URLconf.
* Started SearchView tests and added URLconf.
* Added note about basic use. Needs refactoring.
* Merged index.rst.
* Fixed result lookups when constructing a SearchResult.
* Added more docs.
* Added FIXME for exploration on Solr backend.
* Solr's SearchQuery now handles phrases (exact match).
* More work on the Solr backend.
* Added more imports for future test coverage.
* Added stubs for backend tests.
* Documentation updates.
* Refactored forms/views. Needs tests.
* Removed old entries in .gitignore.
* Implemented load_all.
* Fixed query result retrieval.
* Updated documentation index and tweaked overview formatting.
* Slight docs improvements.
* Started work on Solr backend.
* Ignore _build.
* Refactored documentation to format better in Sphinx.
* Added _build to .gitignore.
* Added sphinx config for documentation.
* Verified _fill_cache behavior. 100% test pass.
* Added a couple new desirable bits of functionality. Mostly stubbed.
* Removed fixme and updated docs.
* Removed an old reference to SearchPaginator.
* Updated import paths to new backend Base* location.
* Relocated base backend classes to __init__.py for consistency with Django.
* BaseSearchQuerySet initial API complete and all but working. One failing test related to caching results.
* Added new (improved?) template path for index templates.
* Removed SearchPaginator, as it no longer provides anything over the standard Django Paginator.
* Added len/iter support to BaseSearchQuerySet. Need to finish getitem support and test.
* Started to update ModelIndex.
* Started to alter dummy to match new class names/API.
* Little bits of cleanup.
* Added overview of where functionality belongs in djangosearch. This should likely make it's way into other docs and go away eventually.
* BaseSearchQuery now tracks filters via QueryFilter objects. Tests complete for QueryFilter and nearly complete for BaseSearchQuery.
* Started docs on creating new backends.
* Started tests for BaseSearchQuery and BaseSearchQuerySet.
* Fixed site loading.
* More work on the Base* classes.
* Started docs on creating new backends.
* Yet more work on BaseSearchQuerySet. Now with fewer FIXMEs.
* More work on BaseSearchQuerySet and added initial BaseSearchQuery object.
* Removed another chunk of SearchPaginator as SearchQuerySet becomes more capable. Hopefully, SearchPaginator will simply go away soon.
* Fixed ModelSearchForm to check the site's registered models.
* Reenabled how other backends might load.
* Added ignores.
* Started documenting what backends are supported and what they can do.
* More work on SearchQuerySet.
* More renovation and IndexSite's tests pass 100%.
* Fleshed out sites tests. Need to setup environment in order to run them.
* Started adding tests.
* First blush at SearchQuerySet. Non-functional, trying to lay out API and basic funationality.
* Removed old results.py in favor of the coming SearchQuerySet.
* Noted future improvements on SearchPaginator.
* Removed old reference to autodiscover and added default site a la NFA.
* Commented another use of RELEVANCE.
* Little backend tweaks.
* Added autodiscover support.
* Readded management command.
* Added SearchView and ModelSearchForm back in. Needs a little work.
* Readded results. Need to look at SoC for ideas.
* Readded paginator. Needs docs/tests.
* Readded core backends + solr. Will add others as they reach 100% functionality.
* Added ModelIndex back in. Customized to match new setup.
* Added signal registration as well as some introspection capabilities.
* Initial commit. Basic IndexSite implementation complete. Needs tests.
