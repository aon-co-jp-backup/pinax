---
layout: post
title: "django-avatar 1.0.4 Release Notes"
date: 2010-03-16 01:19:09
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-avatar/django-avatar-1.0.4.tar.gz>

This release includes the following:

* Merge branch 'master' of git://github.com/ericflo/django-avatar
* More obsessive compulsiveness
* Obsessive compulsive import cleanup
* Cleanup, reorganization, moved the default avatar url to conform to community standards, and added a test to ensure that it's correct.
* Cleanup, reorganization, moved the default avatar url to conform to community standards, and added a test to ensure that it's correct.
* Remove vestigial import
* Moved default.jpg to reflect the community standard for media files
* Add a clarifying comment
* Remove an accidental pyc file checkin
* Add a .gitignore
* Added the ability to run the tests in a standalone way.
* Moved template folder to correct name (notification)
* Cleaned up noticetext, removing reference to the user's gender and nonsense regarding tribes
* Use PyFlakes to fix some fail
* Replace hashlib by django's md5_constructor
* Allow extra args that might be sent to the views. Useful with custom URLConf for instance.
* fix resize for render_primary: size is a string, we need to convert it to an integer.
* render_primary() needs AVATAR_DEFAULT_URL
* Fixed conflicts
* Marking added strings for translation and providing a basic french translation
* Lowercase filename just in case.
* Implement a basic file extension validation system.
* Force thumbnail extension if AVATAR_HASH_FILENAMES is true. Avoids having / .jpg images that are really PNGs.
* Use pretty decorators
* More basic tests
* Adding basic tests
* Oops.
* Implement filename hashing (in case we don't want to blindly accept the filenames supplied by the user) and directory hashing (to allow / storage paths like /avatars/a/b/<user>/...)
* Will revisit that later, it's not a big issue
* Thumbnails path simplification - /AVATAR_STORAGE_DIR/<user>/resized/<size>/<name> is enough. And this / method is more DRY, which will help when we'll implement the advanced storage path stuff
* This time it should really work in every case... I hope. This really needs some unit tests.
* irrelevant now
* This was needed too - basically, only enforce AVATAR_MAX_AVATARS_PER_USER in the form.
* use the user from the avatar instance
* Simplify image handling. Breaks the new AVATAR_DONT_SAVE_DUPLICATES setting but I will revisit it later in a cleaner way
* Actually not a good idea at all :) Just don't bother updating and that's it.
* is a boolean
* if AVATAR_DONT_SAVE_DUPLICATES is enabled don't generate a thumbnail over an existing one
* new preference allowing to re-use existing file if it exists. might have concurrency issues since / we don't ask the database if it exists, only the storage system, so it might break if it's being / deleted at the same time
* Make thumbnail format configurable
* Don't use only(id) now that we are deleting instead of updating
* Deleting instead of updating for now
* debugging, not needed
* This method is more closer to the original and should be more robust even if you change the max number of avatars
* Oops, need to actually get the first item of the queryset
* More robust way of fetching the current avatar - still needs some testing
* Better wording
* Don't use notification if the module is not present (probably broke that when refactoring notifications)
* Implement a max size for the avatars. Defaults to 1 megabyte for now.
* Useless print
* Not needed
* Fixed now
* Use our uploadform in the templates
* special case for AVATAR_MAX_AVATARS_PER_USER == 1: try to work always on the same db row, by re-using the id.
* Raise an error if trying to upload an avatar when the maximum number was already reached
* Forgot this in my last commit - Refactoring : Move avatar upload to its own view, form and template part 2
* Refactoring : Move avatar upload to its own view, form and template. Needs some cleanup still. /  / I should have done this before adding the max avatars setting... oh well.
* Don't update the other avatars if the maximum is set to 1: it shouldn't happen.
* Starting to implement new AVATAR_MAX_AVATARS_PER_USER setting to limit the maximum number of avatars for each user
* Don't use multiple querysets for the same list (might revisit the .get() for avatar later)
* Ignore pyc files
* Fixed #586 - Added login_required to avatar.views.delete
* Provide Gravatar default url in settings.AVATAR_GRAVATAR_DEFAULT - will be used by Gravatar if the user has no avatar for that email address.
* Fix for error in django-avatar 1.0.3 (task #524).
