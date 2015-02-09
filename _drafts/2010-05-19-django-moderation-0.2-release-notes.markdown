---
layout: post
title: "django-moderation 0.2 Release Notes"
date: 2010-05-19 22:46:26
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-moderation/django-moderation-0.2.tar.gz>

This release includes the following:

* Added info about 0.2 release.
* Added settings list in to README
* Refactored setUp and tearDown methods of some TestCases.
* Added contributors list
* Added option bypass_moderation_after_approval in to GenericModerator class that will release object from moderation system after initial approval of object. Closes #17
* Fixed typo in is_auto_reject method. Thank you Jon.
* Code refactoring of GenericModerator class methods is_auto_approve and is_auto_reject
* Added ability to provide custom auto reject/approve reason. Closes #16
* Code rafactoring
* Fixed test test_content_types to be more generic.
* Fixed issue with multiple save of changed object.
* Added example how to define custom login in auto moderation.
* Added possibility of passing changed object in to is_auto* methods of GenericModerator class. This will allow more useful custom auto-moderation. Ex. auto reject if akismet spam check returns True. Closes #15
* Fixed imports of test tools used in tests. Now test can be run when tools like: mock, pep8 are not istalled but this tests will not pass until its installed. Closes #9
* Fixed issue when creating model forms for objects that doesnt have moderated object created. Thank you signal. Closes #13
* Added admin filter that will show only content types registered with moderation in admin queue. Closes #12
* Removed unnecessary import
* Added test helper functions to setup moderation registration in tests
* Fixed issue with multible model save when automoderate was used. Auto moderation in save method of ModeratedObject has been moved to seperate method. Closes #11
* Fixed issue when more then one model is registered with moderation and multiple model instances have the same pk.
* Fixed issue with accessesing objects that existed before installation of django-moderation on model class. Closes #13
* Fixed issue with TypeError when generating diff of changes between model instances that have field with non unicode value ex. DateField. Fixed typo in method name. Closes #6
* Fixed spell error
* Merge branch 'master' of github.com:dominno/django-moderation
* Fixed issue when loading object from fixture for model class that is registered with moderation. Now moderated objects will not be created when objects are loaded from fixture.
* Fixed deprecation warning for django 1.2
* Fixed typo in README
* Fixed import. Fixes issue #10
* Added csrf_token. Fixes issue #5. Thank you jonwd7.
* Fixed send_message method. Fixes issue #7
* Aded info about overwriting save_model method of ModelAdmin. Fixes issue #8
* Merge branch 'master' of github.com:dominno/django-moderation
* Moved test_settings.py in to module settings in tests module.
* Code refacotring - removed notifications module. Funtionality was moved to GenericModerator class.
* Fixed typo in README
* Code refactoring, removed notifications.py and tests for them, code has been moved in to GenericModerator class
* Added info about automoderate function helper
* Added tests for automoderate helper function
* Changed name of testcase
* Changed moderated_object property in ModerationManager class, moderated object is geted only once from database, next is cached in _moderated_object, fixed issue with not setting user object on changed_by atrr of ModeratedObject model
* Changed order of checking for automoderate, fixed issue with multiple saving of moderate object.
* Added automoderate helper in to admin save_model method
* Added automoderate helper function
* Fixed typo in ModeratedObject db column. Warning this change, changes DB column. Fixes issue #4
* Fixed typo, fixes issue #3
* Removed django-test-extensions, added mock.
* Fixed informing user when object is moderated
* Fixed get_object_for_this_type method of ModeratedObject model
* Fixed info how to run tests
* Fixed typo.
* Added information about 0.1.1 release
* Added information how to configure GenericModerator class when registering model class with moderation.
* Added automoderation in to save method of ModeratedObject model class
* Chnaged order of checking for auto approve
* Added tests for auto approve and auto reject
* Added options to GenericModerator class: auto_approve_for_superusers, auto_approve_for_staff, auto_approve_for_groups, auto_reject_for_anonymous, auto_reject_for_groups. Added methods for checking auto moderation
* Added tests for is_auto_reject and is_auto_approve methods
* Added saving information who changed object in save_model method, removed checking of 'admin_integration_enabled'
* Added get_moderator method
* Added test for get_moderator method
* Added GenericModerator class that encapsulates moderation options for a given model. Chnaged register method, it  will get only two parameters: model class and settings class. Added option to register models with multiple manager.
* Removed ModerationInfo class from managers tests
* Added test models for register model class with multiple managers
* Added test case for registration with multiple managers, removed tests for class ModerationInfo
* Added tests for GenericModerator class
* Fixed LICENSE typo.
* Removed info "not tested on Django 1.2" - all tests for django 1.2 pass
* Changed object variables to obj, thank you Jon for sugestion.
* Fixed typo moderatated_by - moderated_by. Thank you Jon.
* Added info to README - how to run tests for django-moderation
* Fixed typo in README
* Added testcase and regresion testcase for db integrity error when saving model with unique field. Thank you apollo13.
* Fixed SerializationTestCase to pass on Django 1.2
* Fixed BaseModeratedObjectForm tests to pass on django 1.2
* Fixed code formating to pass PEP8 test
* Fixed filter_moderated_objects method of ModerationObjectsManager to work with Django 1.2
* Added test case for django 1.2 into buildout.cfg
* Chnaged extension of README file
* Fixded errors in rst README, added Known issues and Road map sections
* Added txt version of README
* Removed README.txt
* Changed extension of README file
* Initial commit
