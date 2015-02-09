---
layout: post
title: "django-haystack 2.0.0 Release Notes"
date: 2013-05-12 05:06:01
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-haystack/django-haystack-2.0.0.tar.gz>

This release includes the following:

* Update solr schema template to fix stopwords_en.txt relocation /  / Seems that in versions >3.6 and >4 stopwords_en.txt moved / to a new location. This won't be backwards compatible for / older versions of solr. /  / Addresses issues #558, #560 / In addition, issue #671 references this problem
* Merge branch 'master' of github.com:toastdriven/django-haystack
* Be a bit more careful when resetting connections in the multiprocessing updater. Fixes #562.
* Tests: mark expected failures in Whoosh suite /  / This avoids making it painful to run the test suite and flags the tests which / need attention
* Tests: mark expected failures in ElasticSearch suite /  / This avoids making it painful to run the test suite and flags the tests which / need attention
* multiple index tests: correct handling of Whoosh teardown /  / We can't remove the Whoosh directory per-test - only after every / test has run…
* Whoosh tests: use a unique tempdir /  / This ensures that there's no way for results to persist across runs / and lets the OS clean up the mess if we fail catastrophically /  / The multiindex and regular whoosh tests will have different prefixes to ease / debugging
* test runner: set exit codes on failure
* tox: refactor envlist to include Django versions /  / * Expanded base dependencies / * Set TEST_RUNNER_ARGS=-v0 to reduce console noise / * Add permutations of python 2.5, 2.6, 2.7 and django 1.3 and 1.4
* test runner: add $TEST_RUNNER_ARGS env. variable /  / This allows you to export TEST_RUNNER_ARGS=-v0 to affect all 9 / invocations
* tox: store downloads in tmpdir
* Fixed distance handling in result parser of the elasticsearch backend. This is basically the second part of #566. Thanks to Josh Drake for the initial patch.
* Added ericholscher to AUTHORS.
* Add a title for the support matrix so it's linkable.
* Tests for update_index timezone support /  / * Confirm that update_index --age uses the Django timezone-aware now /   support function / * Skip this test on Django 1.3
* Tests: command-line help and coverage.py support /  / This makes run_all_tests.sh a little easier to use and simplifies the process of / running under coverage.py /  / Closes #683
* Add a CONTRIBUTING.md file for Github /  / This is a migrated copy of docs/contributing.rst so Github can suggest it when / pull requests are being created
* Fix combination logic for complex queries /  / Previously combining querysets which used a mix of logical AND and OR operations / behaved unexpectedly. /  / Thanks to @mjl for the patch and tests in SHA: 9192dbd /  / Closes #613, #617
* update_index: use tz-aware datetime where applicable /  / This will allow Django 1.4 users with USE_TZ=True to use update_index with time / windowing as expected - otherwise the timezone offset needs to be manually / included in the value passed to -a
* Added rz to AUTHORS.
* Fixed string joining bug in the simple backend.
* Added failing test case for #438.
* Tests: basic help and coverage.py support /  / run_all_tests.sh now supports --help and --with-coverage
* Fix Solr more-like-this tests (closes #655) /  / * Refactored the MLT tests to be less brittle in checking only /   the top 5 results without respect to slight ordering /   variations. / * Refactored LiveSolrMoreLikeThisTestCase into multiple tests / * Convert MLT templatetag tests to rely on mocks for stability /   and to avoid hard-coding backend assumptions, at the expense /   of relying completely on the backend MLT queryset-level tests /   to exercise that code. / * Updated MLT code to always assume deferred querysets are /   available (introduced in Django 1.1) and removed a hard-coded /   internal attr check
* All backends: fixed more_like_this & deferreds /  / Django removed the get_proxied_model helper function in the 1.3 dev / cycle: /  / https://code.djangoproject.com/ticket/17678 /  / This change adds support for the simple new property access used by 1.3+ /  / BACKWARD INCOMPATIBLE: Django 1.2 is no longer supported
* Elasticsearch geo_bounding_box filter expects top_left (northwest) and bottom_right (southeast). / Haystack's elasticsearch backend is passing northeast and southwest coordinates instead.
* Fixes incorrect call to put_mapping on elasticsearch backend
* Updated elasticsearch backend to use a newer pyelasticsearch release that features an improved API , connection pooling and better exception handling.
* Added Gidsy to list of who uses Haystack.
* Increased the number of terms facets returned by the Elasticsearch backend to 100 from the default 10 to work around an issue upstream. /  / This is hopefully only temporary until it's fixed in Elasticsearch, see https://github.com/elasticsearch/elasticsearch/issues/1776.
* Added Pitchup to Who Uses.
* Merge branch 'unittest2-fix'
* Better unittest2 detection /  / This supports Python 2.6 and earlier by shifting the import to look / towards the future name rather than the past
* Add a minimal .travis.yml file to suppress build spam /  / Until the travis-config branch is merged in, this can be spread around to avoid / wasting time running builds before we're ready
* Tests: enable Solr content extraction handler /  / This is needed for the test_content_extraction test to pass
* Tests: Solr: fail immediately on config errors
* Solr tests: clean unused imports
* Suppress console DeprecationWarnings
* Update unittest2 import logic /  / We'll try to get it from Django 1.3+ but Django 1.2 users will need to install / it manually
* Fix typo
* Fixed logging in simple_backend.
* Refactor to use a dummy logger that lets you turn off logging
* A bunch of Solr testing cleanup.
* Skip test is pysolr isn't available
* Updated Who Uses to correct a backend usage.
* Updated documentation about using the main pyelasticsearch release.
* Missing `
* Fixed a mostly-empty warning in the ``SearchQuerySet`` docs. Thanks to originell for the report!
* Fixed the "Who Uses" entry on AstroBin.
* Use the match_all query to speed up performing filter only queries dramatically.
* Fixed typo in docs. Closes #612.
* Updated link to celery-haystack repository.
* Fixed the docstring of SearchQuerySet.none. Closes #435.
* Fixed the way quoting is done in the Whoosh backend when using the / ``__in`` filter.
* Added the solrconfig.xml I use for testing.
* Fixed typo in input types docs. Closes #551.
* Make sure an search engine's backend isn't instantiated on every call to the backend but only once. Fixes #580.
* Restored sorting to ES backend that was broken in d1fa95529553ef8d053308159ae4efc455e0183f.
* Prevent spatial filters from stomping on existing filters in ElasticSearch backend.
* Merge branch 'mattdeboard-sq-run-refactor'
* Merge branch 'master' of https://github.com/toastdriven/django-haystack
* Fixed an ES test that seems like a change in behavior in recent ES versions.
* Merge branch 'sq-run-refactor' of https://github.com/mattdeboard/django-haystack into mattdeboard-sq-run-refactor
* Merge branch 'master' of https://github.com/toastdriven/django-haystack
* Refactor Solr & ES SearchQuery subclasses to use the ``build_params`` from ``BaseSearchQuery`` to build the kwargs to be passed to the search engine. /  / This refactor is made to make extending Haystack simpler. I only ran the Solr tests which invoked a ``run`` call (via ``get_results``), and those passed. I did not run the ElasticSearch tests; however, the ``run`` method for both Lucene-based search engines were identical before, and are identical now. The test I did run -- ``LiveSolrSearchQueryTestCase.test_log_query`` -- passed.
* Fixed Django 1.4 compatibility. Thanks to bloodchild for the report!
* Refactored ``SearchBackend.search`` so that kwarg-generation operations are in a discrete method. /  / This makes it much simpler to subclass ``SearchBackend`` (& the engine-specific variants) to add support for new parameters.
* Merge branch 'master' of github.com:jezdez/django-haystack
* Added witten to AUTHORS.
* Fix for #378: Highlighter returns unexpected results if one term is found within another.
* Removed jezdez's old entry in AUTHORS.
* Added Jannis to Primary Authors.
* Add missing `ImproperlyConfigured` import from django's exceptions. /  / l178 failed.
* Fixed ``SearchIndex.get_model()`` to raise exception instead of returning it.
* Commercial support is now officially available for Haystack.
* Fixed update_index process leak.
* Using multiple workers (and resetting the connection) causes things to break when the app is finished and it moves to the next and does qs.count() to get a count of the objects in that app to index with psycopg2 reporting a closed connection. Manually closing the connection before each iteration if using multiple workers before building the queryset fixes this issue.
