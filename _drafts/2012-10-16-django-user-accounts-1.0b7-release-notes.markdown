---
layout: post
title: "django-user-accounts 1.0b7 Release Notes"
date: 2012-10-16 01:33:08
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-user-accounts/django-user-accounts-1.0b7.tar.gz>

This release includes the following:

* Bumped version for next release
* Moved version string to a more universal location
* Call SignupView.after_signup before sending email confirmation /  / There are many cases where the after_signup hook needs to setup data from the / form that may affect what is displayed in the confirmation email. By moving / the email confirmation send after we call after_signup a site developer can / build a more personalized email confirmation email.
* Added EmailAddress object to confirmation email context
* Gets empty string as default for redirect_field_name /  / Both the empty string and None evaluate to not true, but None will be / displayed as "None" in a template. This obviates the need for template / conditionals to display or not display the next value.
* Moved load_path_attr before AccountAppConf /  / This is needed due to AppConf calling methods as soon as the class is created.
* Added missing import in account.middleware
* Fixed recursive import with load_path_attr /  / account.utils wants account.conf and account.conf wants account.utils. This / commits fixes that by moving load_path_attr into account.conf. /  / Thanks natmaster for detecting this early in the morning.
* Update docs/migration.rst /  / Add MySql SQL migration.
* Updated docs for recent API change
