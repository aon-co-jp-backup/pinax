---
layout: post
title: "django-user-accounts 1.0c6 Release Notes"
date: 2014-05-23 19:22:21
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-user-accounts/django-user-accounts-1.0c6.tar.gz>

This release includes the following:

* Bumped version for next RC
* Setup signup_code in a consistent manner
* Bumped version for next RC
* Fixed current_site bug in SignupCode.send
* Bumped version for next RC
* Moved signup code lookup to own method
* Bumped version for next RC
* Changed version to RC (not quite 1.0 yet)
* Allow custom signup_url in SignupCode.send
* Added extra_ctx to SignupCode.send /  / Callers of SignupCode.send can now pass through extra context to the template.
* Follow brosner's advice re: cleaning up the new text.
* Document what to do about account_account pk conflicts from fixtures.
* Write django-user-accounts instead of d-u-a /  / While reading the FAQ I stumbled over `d-u-a`. I hadn't seen it anywhere in the documentation. I searched the term before realizing it was `django-user-accounts`. (Duh.) I propose you spell it out and save the next person some confusion. Alternatively, consider referring to the project as `d-u-a` throughout for consistency.
* updated spanish translation with last transifex file (by nqnwebs -- me --)
* add translations
* add Meta
* Added nl source files
* Bumped version to 1.0
* Renamed SignupCode.check to check_code /  / This change is BACKWARD INCOMPATIBLE if you relied on SignupCode.check in your / own code. The change is required for 1.7 support. /  / Django 1.7 introduces a new check framework which works from Model.check and / clashed with our SignupCode.check. /  / Refs #113
* Fixed import on 1.7+ /  / Refs #113
