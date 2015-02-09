---
layout: post
title: "pinax-points 0.1 Release Notes"
date: 2015-01-24 01:46:43
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/p/pinax-points/pinax-points-0.1.tar.gz>

This release includes the following:

* upgrade and rename to pinax-points
* Fix white space issue
* Fix lint errors
* Add travis
* 0.1.dev23
* Update for latest Django
* Update LICENSE years
* 0.1.dev22
* Add user_has_voted template tag
* 0.1.dev21
* Add ability to prevent negative totals
* a few bug fixes
* added voting
* let caller deal with queryset limiting on their own
* 0.1.dev18
* changed get_ to fetch_
* 0.1.dev17
* abstracted out queryset logic for top_objects to a function
* 0.1.dev16
* fixed bug not accounting for users with no points
* 0.1.dev15
* fixed fencepost error
* 0.1.dev14
* raise NotImplementedError for non auth.User objects
* implemented time limits param on top_objects for auth.User only at the moment
* bump version
* added support for time limits on points_for_object
* added package_data for installing templates
* added breadcrumbs to one-off points interface and redirect to changelist after awarding
* added customized change_list.html template for linking to one-off points
* hook up giving a reason for one-off points
* added interface to one-off point awards
* bumped to 0.1.dev10
* added field for custom reason (largely for one-off points)
* added admin.py for models
* bumped to 0.1.dev9
* Merge branch 'one-off-plus-objects'
* fixed points_awarded docstring
* fixed bug with lookup_params building in points_awarded
* removed the protection when target was optional in points_awarded
* removed source on TargetStat
* corrected incorrect use of a tuple
* minor clean-ups
* super awesome test running - thanks carl
* Merge branch 'track-related-object' into one-off-plus-objects /  / Conflicts: / 	agon/models.py / 	agon/signals.py / 	agon/tests.py
* add ability to allow awarding points on a one off basis
* added support for tracking source objects on points awarded
* removed unused import and variable
* bump to 0.1.dev8
* __unicode__ methods for PointValue and AwardedPointValue
* added support for seven arguments in top_objects and points_for_object (to be implemented later) for seventh development release /  / Q: how funny is this? / A: 7
* 0.1.dev6
* Merge branch 'master' of github.com:eldarion/agon
* Order by position *ascending* lower position is better.
* 0.1.dev5
* Implemented points_for_object and fixed points_awarded for objects that don't have points yet.
* Can't filter after slice.
* Fix a nameerror
* Fix instantiation.
* 0.1.dev3
* Fix template tag (it had an impossible condition in it.
* added agon.templatetags and bumped version
* added `top_objects` template tag
* added PointValue.create for creation of point values
* moved point values to the database to support dynamic point values
* added positions calculation
* A style nit of my own.
* fixed a typo in non-User case of awarding points with test case to prove it works
* we do things to my liking
* better name for a subclassed class of TransactionTestCase
* whitespace patrol again
* Fix transactional issues.
* white space patrol
* Added skipIf decorator, it's not perfect since it doesn't tell you a test was skipped, but meh.
* minor clean-ups
* Test isolation.
* Consolidate testing infastructure, also skip the broken test.
* More tests
* fixed name overlapping
* added points_awarded to return the number points the given target has
* test improper configuration
* added missing import
* better abstraction and ensure update_points is called when IntegrityError is raised
* fixed incorrect field name after TargetStat addition
* ensure TargetStat is created when it does not exist in award_points
* TargetPointTotal -> TargetStat — paved the way for positions and levels
* stubbed out TargetPointTotal.full_calculate
* fire off points_awarded signal when points are awarded
* added .gitignore
* added MANIFEST.in
* corrected extension in setup.py for README
* changed extension of README to render as restructured text
* updated README
* added docstring to award_points
* initial take on models.py with models and award_points written out
* added LICENSE
* added setup.py
* Python package
* initial commit
