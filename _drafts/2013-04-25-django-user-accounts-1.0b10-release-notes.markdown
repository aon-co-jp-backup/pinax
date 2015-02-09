---
layout: post
title: "django-user-accounts 1.0b10 Release Notes"
date: 2013-04-25 18:25:57
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-user-accounts/django-user-accounts-1.0b10.tar.gz>

This release includes the following:

* Bumped version
* Added SignupView.create_email_address /  / This commits moves the logic for creating the EmailAddress object to its own / method. Site developers can now override the behavior of the creation of this / object without having to redefine SignupView.form_valid.
* Bumped version
* Added ConfirmEmailView.after_confirmation /  / This new method allows site developers to override the behavior after a user / has confirmed their email address. By default, it will mark the User object / active.
