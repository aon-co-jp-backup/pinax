---
layout: post
title: "django-avatar 1.0.5 Release Notes"
date: 2010-06-24 21:19:03
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-avatar/django-avatar-1.0.5.tar.gz>

This release includes the following:

* Merge remote branch 'alex/master'
* Removed superflous code.
* Merge branch 'master' of git://github.com/alex/django-avatar
* Do significantly fewer SQL queries here.
* Fixes for Django 1.2
* Bumped version given latest changes.
* The default avatar URL could also start with https.
* AVATAR_DEFAULT_URL can start with http:// if for some reason it's hosted on another domain /  / Signed-off-by: Jannis Leidel <jannis@leidel.info>
* Fix redirect to only happen if the "add" action was successful. It was already breaking unit tests, but add more to be sure. /  / Signed-off-by: Jannis Leidel <jannis@leidel.info>
* FR translation .mo /  / Signed-off-by: Jannis Leidel <jannis@leidel.info>
* French translations update /  / Signed-off-by: Jannis Leidel <jannis@leidel.info>
* Use django 1.2 CSRF protection /  / Signed-off-by: Jannis Leidel <jannis@leidel.info>
* Fix for issue #12 on ericflo/django-avatar, proposed by fakeempire /  / Signed-off-by: Jannis Leidel <jannis@leidel.info>
* Bumped to 1.1a2.
* Merge branch 'master' of git://github.com/ericflo/django-avatar
* Added redirect to add view to be able to add an image from a different URL/template without landing on the add template afterwards.
* Merge remote branch 'jezdez/master'
* Added default image to source distribution.
* Merge remote branch 'jezdez/master' /  / Conflicts: / 	setup.py
* Handle non-ASCII filenames correctly when hashing the filename.
* Merge branch 'master-old'
* Added translations to source distribution.
* Added German translation.
* Marked a few strings for translation.
* Added thumb quality setting which is used in the create_thumbnail() method.
* Added Portuguese (Brazilian) translation. /  / Signed-off-by: Jannis Leidel <jannis@leidel.info>
* adding default quality param to create_thumbnail /  / Signed-off-by: Jannis Leidel <jannis@leidel.info>
* More unit tests.
* FIXME: more tests that need to be coded /  / Signed-off-by: Jannis Leidel <jannis@leidel.info>
* Test get_primary_avatar behaviour /  / Signed-off-by: Jannis Leidel <jannis@leidel.info>
* Fixed issue #7: get_primary shouldn't return urls, it should return objects (or just None in that case) /  / Signed-off-by: Jannis Leidel <jannis@leidel.info>
* Bump to an imaginary 1.1a1 release.
* Allow overriding the upload and primary avatar form via a view parameter. Also don't set the default of the extra_context parameter in the function declaration.
* Don't rely on the Django app cache's get_app() since it's not guaranteed to find the app whe django-avatar is loaded.
