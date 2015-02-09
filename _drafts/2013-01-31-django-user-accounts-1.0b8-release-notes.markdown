---
layout: post
title: "django-user-accounts 1.0b8 Release Notes"
date: 2013-01-31 05:49:31
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-user-accounts/django-user-accounts-1.0b8.tar.gz>

This release includes the following:

* Bumped version for next release
* Fixed user state bug during sign up when sign up code is used /  / When a user signs up with a sign up code we check if the given email matches the / sign up code email. If they match we confirm the email, but we don't reactivate / the user account when ACCOUNT_EMAIL_CONFIRMATION_REQUIRED is True. /  / This commit fixes this ensuring users are activated correctly when they never / receive the email confirmation by design.
* Added CONTRIBUTING documentation to repository
* Updated to latest pytz
* Fixed small bug in after_change_password /  / Defined missing user variable after a previous minor code refactor. /  / Fixes #56 — thanks swiharta for the bug report.
* Update migration docs
* Unify and isolate password changes in password change views /  / ChangePasswordView and PasswordResetTokenView both change the password of the / acting user. Their APIs are now unified. /  / ChangePasswordView used to rely on the form to set the user's password. This / has been moved to the view as the correct place for this behavior. This is / backwards incompatible for forms that overrode ChangePasswordForm.save to / modify the password setting behavior. /  / PasswordResetTokenView has been unified with the new API given to / ChangePasswordView. The password_changed signal is now fired from the view / when the password is changed. /  / The new API now isolates the password change behavior from actions to take / after the password has been changed on the User model or any other behavior / a site developer needs to take when password is being changed.
* Fix documentation error
* Merge branch 'binarymac-master'
* Listed templates that are required by default
* Update sphinx conf and Makefile
* Fix signals documentation
* Fixed migration docs formatting
* Removed successfully logged in user message /  / This message isn't entirely useful and adds to the user experience in a bad / way by default. If a site wants to maintain this user message it can be done / with an custom subclass of SignupView.
