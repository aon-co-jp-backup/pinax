---
layout: post
title: "django-moderation 0.3.2 Release Notes"
date: 2012-02-15 22:30:26
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-moderation/django-moderation-0.3.2.tar.gz>

This release includes the following:

* Added info about version 0.3.2 in history file
* Fixed PEP8 code formatting
* fixed xss vulnerability
* Added sorting of content types list on admin moderation queue
* Fixed usage of package as egg, required by south. CLoses #42
* Fixed PEP8 code formatting
* Added info about project CI system
* Fixed PEP8 code formatting
* Fixed non passing test - test_filter_moderated_objects_returns_empty_queryset
* Fixed SMTPRecipientsRefused when user has no email, when sending messages by moderation. Closes #48
* Added test command that launch tests for all supported versions of Django.
* Added fix to maintain backward compatibility with django 1.1.X
* Fixed visibility_column and visible_until_rejected functionality. Was not working when both were set.
* Fixed tests for fields exclude
* Fixed tests for diff operations and for _get_or_create_moderated_object method
* Refactored solution for issue #43
* Fixed tests for case when user access object in admin and it doesnt have moderated_object associated but model is registered with moderation.
* Added Django 1.3.1 to testable Django versions
* Added treyhunner to contributors list. Thank you.
* Fix visible_until_rejected merge error
* Fix spelling error
* Merge branch 'topic/fix-automoderate'
* Merge branch 'topic/takedown-support' /  / Conflicts: / 	src/moderation/admin.py / 	src/moderation/register.py
* Add ``visible_until_rejected`` usage to README
* Render unicode strings properly
* Fixed bug with admin throwing DoesNotExist exception /  / Signed-off-by: Trey Hunner <treyhunner@gmail.com>
* Merge branch 'topic/moderated-fields-list'
* Simplify test case per advice of @dominno.
* Suppress error when no delete action in admin site
* Fix bug introduced by 74e4ba9edda7ae57008224f7f5bf4bd357e7ecb1
* Do not check for previous versions of newly created objects
* Added connection argument to fields methods
* Narrow try block to only catch targeted exception
* Fix typo about admin_integration_enabled in README
* Update tests cases for word-based differencing
* Use word-based diff (instead of character-based)
* Remove README text about foreign keys not being supported (they are now)
* Merge branch 'topic/admin-object-link'
* Merge branch 'topic/foreign-key'
* Add ModerationAdmin message appropriate when visible_until_rejected
* Change version number
* Add test case for moderated_fields class property
* Rename regression test package /  / Fixes error introduced by 88a100297dc0725d9b5d9120a78e096a557b93ca.
* Fix spelling of manager in test_app1 models
* Allow models to specify list of moderated fields
* Force default serializers for test cases
* Fix visible_until_rejected pre_save_handler bug
* Automoderate based on correct version
* Remove spaces around unchanged characters in diff
* Fail gracefully for missing changed_object relations
* Add diff test case for foreign key changes
* Fix diff test cases to include foreign keys
* Allow foreign keys changes
* Merge commit '6f61d570ad'
* Always maintain correct approved object
* Show correct model diff for visible_until_rejected
* Spelling corrections (found using scspell)
* Forms use visible object if visible_until_rejected
* When visible_until_rejected don't save changed_obj on approve
* Allow specific initials in BaseModeratedObjectForm /  / Add test case for BaseModeratedObjectForm includes
* Add support for multi-table inheritance /  / Add multi-table inheritance serialization test
* Fix spelling in tests
* Spelling correction
* PEP8: Fix inline comment spacing
* PEP8: fix missing and extra blank lines
* Add visible_until_rejected moderator bool param
* Updated instance.moderated_object after saving
* Merge branch 'master' of github.com:dominno/django-moderation
* Add link to original on moderated object page
* Fix diff test case for image field
* Add support for multi-table inheritance
* Add support for ImageFields with null=True set
* Add South migrations
* Merge remote branch 'ixc/master'
* Merge remote branch 'Synopsi/master'
* bugfix: field_path parameter was added int FilterSpec
* bugfix: field_path parameter was added int FilterSpec
* Efficiency improvement: get all info needed to filter a queryset in two SQL requests, rather than one for each object in the queryset.
* Fixed wrong import in README.rst. Thank you ysugiura. Closes #25
* Efficiency improvement: get all info needed to filter a queryset in two SQL requests, rather than one for each object in the queryset.
* Updated info about configuration
* Added test that tests register of model with moderation with use of custom GenericModerator class.
* Removed force module reload
* Updated example project
* Added auto_discover function that discover all modules that contain moderator.py module and auto registers all models it contain with moderartion.  /  / Refacored tests structure.
* Added import do README
* Moved ModerationManager class to moderation.register module, moved GenericModerator class to moderation.moderator module.
* Refactored test structure
* Merge branch 'master' of github.com:dominno/django-moderation
* Merge remote branch 'r1/master'
* Added possibility of excluding fields from moderation change list. Closes #23
* make moderation work with south and grappelli
* make moderation work with south and grappelli
* Added support for ImageField model fields on moderate object page.
* Added visibility_column option in to GenericModerator class. Boost performance of database queries when excluding objects that should not be available publicly. Field must by a BooleanField. The manager that decides which model objects should be excluded when it were rejected, will first use this option to properly display (or hide) objects that are registered with moderation. Use this option if you can define visibility column in your model and want to boost performance. By default when accessing model objects that are under moderation, one extra query is executed per object in query set to determine if object should be excluded from query set. This method benefit those who do not want to add any fields to their Models. Default: None. Closes #19
* Removed setup.cfg
* Changed zip_safe
* Added django 1.2 in to buildout.cfg
* Fixed rst formating
