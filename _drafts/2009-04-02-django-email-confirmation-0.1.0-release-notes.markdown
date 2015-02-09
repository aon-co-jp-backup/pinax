---
layout: post
title: "django-email-confirmation 0.1.0 Release Notes"
date: 2009-04-02 03:26:42
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-email-confirmation/django-email-confirmation-0.1.0.tar.gz>

This release includes the following:

* Moved template to the correct location /  / git-svn-id: http://django-email-confirmation.googlecode.com/svn/trunk@48 e143efbd-a74b-0410-b764-bd10452ab0ba
* Added simple setup.py /  / git-svn-id: http://django-email-confirmation.googlecode.com/svn/trunk@47 e143efbd-a74b-0410-b764-bd10452ab0ba
* Moved email templates to the app itself /  / git-svn-id: http://django-email-confirmation.googlecode.com/svn/trunk@46 e143efbd-a74b-0410-b764-bd10452ab0ba
* Moved emailconfirmation app one level up /  / git-svn-id: http://django-email-confirmation.googlecode.com/svn/trunk@45 e143efbd-a74b-0410-b764-bd10452ab0ba
* Fixes issue 7 - breakage introduced in r43 /  / git-svn-id: http://django-email-confirmation.googlecode.com/svn/trunk@44 e143efbd-a74b-0410-b764-bd10452ab0ba
* Fixed issue 4 - use named url pattern for confirm_email so it can be overridden /  / git-svn-id: http://django-email-confirmation.googlecode.com/svn/trunk@43 e143efbd-a74b-0410-b764-bd10452ab0ba
* Fix issue 5 - get rid of newlines in email subject, fix indentation and line length /  / git-svn-id: http://django-email-confirmation.googlecode.com/svn/trunk@42 e143efbd-a74b-0410-b764-bd10452ab0ba
* Fixes issue 6 - missing verbose_name_plural /  / git-svn-id: http://django-email-confirmation.googlecode.com/svn/trunk@41 e143efbd-a74b-0410-b764-bd10452ab0ba
* Adjusted the conditional to check for mailer in INSTALLED_APPS explicitly instead of through get_app which isn't safe from a models.py. /  / git-svn-id: http://django-email-confirmation.googlecode.com/svn/trunk@40 e143efbd-a74b-0410-b764-bd10452ab0ba
* Set confirmation e-mails as high priority for django-mailer. /  / git-svn-id: http://django-email-confirmation.googlecode.com/svn/trunk@39 e143efbd-a74b-0410-b764-bd10452ab0ba
* Improved the optional import of django-mailer to rely on INSTALLED_APPS instead of the PYTHONPATH. This also takes the priority kwarg into consideration which is new to django-mailer. /  / git-svn-id: http://django-email-confirmation.googlecode.com/svn/trunk@38 e143efbd-a74b-0410-b764-bd10452ab0ba
* moved .rst to .txt per pinax/django convention /  / git-svn-id: http://django-email-confirmation.googlecode.com/svn/trunk@37 e143efbd-a74b-0410-b764-bd10452ab0ba
* passes now a Site object to the email templates; marked default templates for i18n; /  / git-svn-id: http://django-email-confirmation.googlecode.com/svn/trunk@36 e143efbd-a74b-0410-b764-bd10452ab0ba
* first attempt at rst docs to be used by sphinx /  / git-svn-id: http://django-email-confirmation.googlecode.com/svn/trunk@35 e143efbd-a74b-0410-b764-bd10452ab0ba
* fixed issue #3 /  / git-svn-id: http://django-email-confirmation.googlecode.com/svn/trunk@34 e143efbd-a74b-0410-b764-bd10452ab0ba
* really fixed it this time. :) /  / git-svn-id: http://django-email-confirmation.googlecode.com/svn/trunk@33 e143efbd-a74b-0410-b764-bd10452ab0ba
* Fixed up project to be compatible with NFA version of trunk. /  / git-svn-id: http://django-email-confirmation.googlecode.com/svn/trunk@32 e143efbd-a74b-0410-b764-bd10452ab0ba
* added method for getting list of users with a given (verified) email address /  / git-svn-id: http://django-email-confirmation.googlecode.com/svn/trunk@29 e143efbd-a74b-0410-b764-bd10452ab0ba
* Use django.contrib.sites and reverse to generate the activation url in the / confirmation e-mail. It is passed to the context to work best with i18n / templates. /  /  / git-svn-id: http://django-email-confirmation.googlecode.com/svn/trunk@28 e143efbd-a74b-0410-b764-bd10452ab0ba
* use django-mailer if available /  / git-svn-id: http://django-email-confirmation.googlecode.com/svn/trunk@27 e143efbd-a74b-0410-b764-bd10452ab0ba
* use separate EMAIL_DEBUG to determine whether to send email or print to stdout /  / git-svn-id: http://django-email-confirmation.googlecode.com/svn/trunk@26 e143efbd-a74b-0410-b764-bd10452ab0ba
* only send email if not in DEBUG mode, otherwise print message to stdout /  / git-svn-id: http://django-email-confirmation.googlecode.com/svn/trunk@25 e143efbd-a74b-0410-b764-bd10452ab0ba
* added notion of a primary address /  / git-svn-id: http://django-email-confirmation.googlecode.com/svn/trunk@24 e143efbd-a74b-0410-b764-bd10452ab0ba
* added RequestionContext /  / git-svn-id: http://django-email-confirmation.googlecode.com/svn/trunk@23 e143efbd-a74b-0410-b764-bd10452ab0ba
* added view and template for confirming email /  / git-svn-id: http://django-email-confirmation.googlecode.com/svn/trunk@22 e143efbd-a74b-0410-b764-bd10452ab0ba
* removed silly constraint on multiple confirmations /  / git-svn-id: http://django-email-confirmation.googlecode.com/svn/trunk@21 e143efbd-a74b-0410-b764-bd10452ab0ba
* implemented resending of confirmation email /  / git-svn-id: http://django-email-confirmation.googlecode.com/svn/trunk@20 e143efbd-a74b-0410-b764-bd10452ab0ba
* add email new checks for duplicates /  / git-svn-id: http://django-email-confirmation.googlecode.com/svn/trunk@19 e143efbd-a74b-0410-b764-bd10452ab0ba
* added add email form to homepage /  / git-svn-id: http://django-email-confirmation.googlecode.com/svn/trunk@18 e143efbd-a74b-0410-b764-bd10452ab0ba
* minor style changes /  / git-svn-id: http://django-email-confirmation.googlecode.com/svn/trunk@17 e143efbd-a74b-0410-b764-bd10452ab0ba
* added login and logout /  / git-svn-id: http://django-email-confirmation.googlecode.com/svn/trunk@16 e143efbd-a74b-0410-b764-bd10452ab0ba
* added confirmation model and move email sending to it /  / git-svn-id: http://django-email-confirmation.googlecode.com/svn/trunk@15 e143efbd-a74b-0410-b764-bd10452ab0ba
* added svn:ignore for .pyc /  / git-svn-id: http://django-email-confirmation.googlecode.com/svn/trunk@14 e143efbd-a74b-0410-b764-bd10452ab0ba
* added list of email addresses for logged in user with verification status /  / git-svn-id: http://django-email-confirmation.googlecode.com/svn/trunk@13 e143efbd-a74b-0410-b764-bd10452ab0ba
* default from email sample /  / git-svn-id: http://django-email-confirmation.googlecode.com/svn/trunk@12 e143efbd-a74b-0410-b764-bd10452ab0ba
* email confirmation templates /  / git-svn-id: http://django-email-confirmation.googlecode.com/svn/trunk@11 e143efbd-a74b-0410-b764-bd10452ab0ba
* hooked up email address object creation to signup /  / git-svn-id: http://django-email-confirmation.googlecode.com/svn/trunk@10 e143efbd-a74b-0410-b764-bd10452ab0ba
* email address model and manager /  / git-svn-id: http://django-email-confirmation.googlecode.com/svn/trunk@9 e143efbd-a74b-0410-b764-bd10452ab0ba
* added logout link /  / git-svn-id: http://django-email-confirmation.googlecode.com/svn/trunk@8 e143efbd-a74b-0410-b764-bd10452ab0ba
* added signup form and homepage /  / git-svn-id: http://django-email-confirmation.googlecode.com/svn/trunk@7 e143efbd-a74b-0410-b764-bd10452ab0ba
* added app for testing /  / git-svn-id: http://django-email-confirmation.googlecode.com/svn/trunk@6 e143efbd-a74b-0410-b764-bd10452ab0ba
* added admin url /  / git-svn-id: http://django-email-confirmation.googlecode.com/svn/trunk@5 e143efbd-a74b-0410-b764-bd10452ab0ba
* added svn:ignore /  / git-svn-id: http://django-email-confirmation.googlecode.com/svn/trunk@4 e143efbd-a74b-0410-b764-bd10452ab0ba
* initial settings /  / git-svn-id: http://django-email-confirmation.googlecode.com/svn/trunk@3 e143efbd-a74b-0410-b764-bd10452ab0ba
* initial project/app /  / git-svn-id: http://django-email-confirmation.googlecode.com/svn/trunk@2 e143efbd-a74b-0410-b764-bd10452ab0ba
* Initial directory structure. /  / git-svn-id: http://django-email-confirmation.googlecode.com/svn/trunk@1 e143efbd-a74b-0410-b764-bd10452ab0ba
