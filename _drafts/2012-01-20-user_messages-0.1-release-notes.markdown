---
layout: post
title: "user_messages 0.1 Release Notes"
date: 2012-01-20 15:05:31
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/u/user-messages/user-messages-0.1.tar.gz>

This release includes the following:

* preparing for open sourcing
* cleaning up docs for readthedocs
* updating README to include a quick start
* added simply reply flag to message_sent signal
* Add templatetags to setup.py package dirs, and up dev version number
* Added some more docs.
* Added docs
* 0.1.dev4
* Merge branch 'master' of ssh://git.eldarion.com:1382/user_messages
* Added a template filter for getting if a thread is unread
* More moving to eldarion.test
* COnvert to use eldarion.test
* change to better name
* 0.1.dev3
* Fix a bad URL
* Small change
* Added a context processor for inbox count.
* Clean up a bunch of cruft from girl gamer.
* clean-ups
* added entries to .gitignore
* added MANIFEST.in
* renamed README for awesomeness
* updated setup.py to use distutils not setuptools
* prep version for next dev release. it will be epic and beyound
* development version
* added more metadata in setup.py
* Added forgotten file.
* Send a signal on each message that is sent to allow for external customization.
* Added support for multiple recipients for a message.
* Handle the way relational databases work.
* Remove bad use of get_absolute_url
* Spring cleaning.
* Added tests for the unread() method
* Make the form class of the view pluggable.
* Added a classmethod for ordering an iterable of Threads, with tests.
* Added new tests for the methods that were added last night
* Added a first_messag attribute to threads.
* revert the message ordering fix and put it localized
* Order the messages correctly
* Added an unread method to ThreadManager
* Added a class to the content field that we need for GirlGamer, eventually we'll amek this properly pluggable
* 2.4 compat
* Handle the way girlgamer likes to send user ids to the compose page
* Update tests for the URL names we changed to get this to work with girlgamer
* Make some changes to url reverseing.
* Shorter lines == more readable
* One more small test.
* Finish the view tests.
* Added tests for deleting a thread
* Added yet more tests.
* Added tests for preselecting a user on message creation
* Add tests for the GET half of creating a message, also added test template for it.
* more tests
* Add templates for view tests
* more tests and fixes
* a bevy of fixes + support for running the tests until we figure out how to fix nose
* Moved the test file, last time.
* Added initial tests.
* typo fix
* Allow messages between more than 2 people.
* Merge branch 'master' of ssh://git@git.eldarion.com:1382/user_messages
* handle presetting the user on a message create
* pep8
* Add a view for deleting a thread.
* Add a view to send a message
* Add reply support to threads
* Update the read status of a thread when it's viewed
* Merge branch 'master' of ssh://git@git.eldarion.com:1382/user_messages
* Don't let people see threads tehy aren't a part of
* Add initial views
* pep8
* Fix the forms up
* user real words instead of opaque numbers
* Add a related name
* pep8
* resolved merge conflict
* redid the managers to make more sense
* rearchitect to store more data on the thread
* pep8
* Initial models and managers.
* added setup.py
* first commit
