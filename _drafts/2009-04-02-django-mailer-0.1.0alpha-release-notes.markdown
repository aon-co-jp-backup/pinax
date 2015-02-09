---
layout: post
title: "django-mailer 0.1.0alpha Release Notes"
date: 2009-04-02 03:44:06
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-mailer/django-mailer-0.1.0alpha.tar.gz>

This release includes the following:

* Moved to alpha /  / Signed-off-by: Brian Rosner <brosner@gmail.com>
* Fixed issue #21 -- Python 2.6 has a threading.current_thread function so we need to catch the .get_name AttributeError differently. /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@64 09d42984-cf36-0410-8cf8-11b756d0386d
* Updated to lockfile 0.7 (which does not fix issue #21, yet). /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@63 09d42984-cf36-0410-8cf8-11b756d0386d
* Remove import wrapper for force_unicode introduced in r61 /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@62 09d42984-cf36-0410-8cf8-11b756d0386d
* Fixed issue with module level Django import that can break installation in virtualenvs /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@61 09d42984-cf36-0410-8cf8-11b756d0386d
* Fixed typo /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@60 09d42984-cf36-0410-8cf8-11b756d0386d
* Updated docs to check for existence of django-mailer in INSTALLED_APPS setting /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@59 09d42984-cf36-0410-8cf8-11b756d0386d
* Removed non-functional monkey patch and added mail_managers method /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@56 09d42984-cf36-0410-8cf8-11b756d0386d
* Updated description and README /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@55 09d42984-cf36-0410-8cf8-11b756d0386d
* Fixed setup.py and moved conditional monkey patch for the mail_admins replacement out of the way of mailer/__init__.py /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@54 09d42984-cf36-0410-8cf8-11b756d0386d
* Added files for packaging /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@53 09d42984-cf36-0410-8cf8-11b756d0386d
* Removed unneeded views.py /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@52 09d42984-cf36-0410-8cf8-11b756d0386d
* Removed unneeded fixtures and development project /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@51 09d42984-cf36-0410-8cf8-11b756d0386d
* Moved the mailer app one level up /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@50 09d42984-cf36-0410-8cf8-11b756d0386d
* Made send_mail completely signature compatible with Django's send_mail. Fixes issues with django-contact-form. /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@49 09d42984-cf36-0410-8cf8-11b756d0386d
* Added missing import of the thread module /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@48 09d42984-cf36-0410-8cf8-11b756d0386d
* Added smtplib.SMTPSenderRefused to the list of exceptions caught to defer the e-mail. /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@45 09d42984-cf36-0410-8cf8-11b756d0386d
* Fixed a minor bug in the lockfile.py. /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@44 09d42984-cf36-0410-8cf8-11b756d0386d
* Updated lockfile.py to 0.6. /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@43 09d42984-cf36-0410-8cf8-11b756d0386d
* Port of the documentation from the wiki. /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@42 09d42984-cf36-0410-8cf8-11b756d0386d
* Documentation placeholder. /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@41 09d42984-cf36-0410-8cf8-11b756d0386d
* Fixed a relative import in favor of an absolute import. /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@40 09d42984-cf36-0410-8cf8-11b756d0386d
* Fixed the incorrect spelling of MAILER_FOR_CHASH_EMAILS to MAILER_FOR_CRASH_EMAILS. /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@39 09d42984-cf36-0410-8cf8-11b756d0386d
* Exposed priority on the public API for send_mail and mail_admins. /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@38 09d42984-cf36-0410-8cf8-11b756d0386d
* Added some output for when a process is paused. /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@37 09d42984-cf36-0410-8cf8-11b756d0386d
* Added the ability to pause the sending of mail with MAILER_PAUSE_SEND. /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@36 09d42984-cf36-0410-8cf8-11b756d0386d
* Added SMTPAuthenticationError to list of deferring exceptions. /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@35 09d42984-cf36-0410-8cf8-11b756d0386d
* Fixed a stupid mistake with lockfile exceptions. Should work now. /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@34 09d42984-cf36-0410-8cf8-11b756d0386d
* Adding mail_admins replacement using mailer. / Adding conditional monkey patch to django.core.handlers.base to use / mailer mail_adming on chrashes if settings.MAILER_FOR_CHASH_EMAILS is True. /  /  /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@32 09d42984-cf36-0410-8cf8-11b756d0386d
* Added a lock wait timeout. Default behavior is to never wait for the lock. / Fixes issue #8. / Thanks winhamwr for the report and original patch. /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@31 09d42984-cf36-0410-8cf8-11b756d0386d
* Added MAILER_EMPTY_QUEUE_SLEEP as a setting in settings.py that maps to EMPTY_QUEUE_SLEEP. Default is 30 seconds. /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@30 09d42984-cf36-0410-8cf8-11b756d0386d
* Converted the retry_deferred command to use logging. /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@29 09d42984-cf36-0410-8cf8-11b756d0386d
* Replaced all print statements with proper calls on the logging module. Output is backward compatible. /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@28 09d42984-cf36-0410-8cf8-11b756d0386d
* Handle smtplib.SMTPRecipientsRefused and defer the message properly. /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@27 09d42984-cf36-0410-8cf8-11b756d0386d
* Ensure the file lock is always released. Fixes issue #7. /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@26 09d42984-cf36-0410-8cf8-11b756d0386d
* Fixed up project to be compatible with NFA version of trunk. /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@25 09d42984-cf36-0410-8cf8-11b756d0386d
* oops, unused import /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@23 09d42984-cf36-0410-8cf8-11b756d0386d
* use lock file to prevent overlapping send_all calls /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@22 09d42984-cf36-0410-8cf8-11b756d0386d
* encoded printing in utf-8 and placed in try clause /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@19 09d42984-cf36-0410-8cf8-11b756d0386d
* use strings /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@18 09d42984-cf36-0410-8cf8-11b756d0386d
* oops, wrong place /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@17 09d42984-cf36-0410-8cf8-11b756d0386d
* added retry command /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@16 09d42984-cf36-0410-8cf8-11b756d0386d
* now resolves lazy strings as subjects /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@15 09d42984-cf36-0410-8cf8-11b756d0386d
* added svn:ignore /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@14 09d42984-cf36-0410-8cf8-11b756d0386d
* added send_mail custom management command /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@13 09d42984-cf36-0410-8cf8-11b756d0386d
* print message if email deferred /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@12 09d42984-cf36-0410-8cf8-11b756d0386d
* updated README to reflect fact that engine.py now sends email by default /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@11 09d42984-cf36-0410-8cf8-11b756d0386d
* added message deferral on socket exception /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@10 09d42984-cf36-0410-8cf8-11b756d0386d
* added drop-in replacement for core send_mail /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@9 09d42984-cf36-0410-8cf8-11b756d0386d
* added some defaults to the model /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@8 09d42984-cf36-0410-8cf8-11b756d0386d
* use actual core send_mail to send messages /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@7 09d42984-cf36-0410-8cf8-11b756d0386d
* fixed deprecated maxlength /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@6 09d42984-cf36-0410-8cf8-11b756d0386d
* add svn:ignore /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@5 09d42984-cf36-0410-8cf8-11b756d0386d
* moved prioritization out of manager into engine and actually used algorithm that (should) do the right thing /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@4 09d42984-cf36-0410-8cf8-11b756d0386d
* initial implementation of first layer /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@3 09d42984-cf36-0410-8cf8-11b756d0386d
* Initial directory structure. /  / git-svn-id: http://django-mailer.googlecode.com/svn/trunk@1 09d42984-cf36-0410-8cf8-11b756d0386d
