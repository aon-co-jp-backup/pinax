---
layout: post
title: "django-user-accounts 1.0b1 Release Notes"
date: 2012-07-23 10:00:41
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-user-accounts/django-user-accounts-1.0b1.tar.gz>

This release includes the following:

* Updated version to reflect current version
* Added ACCOUNT_DELETION_EXPUNGE_HOURS to context of DeleteView
* Fixed some bugs from previous commit /  / I forgot to add the changes made to the previous commit to make it match / the commit message. This commit fixes that and brings it in-line with what / was described.
* Changed Account.timezone default and added Account.localtime /  / Account.timezone defaults to an empty string. This allows empty to represent / NOT SET and a site developer can use this to ask for user to set their account / timezone. An empty is handled with settings.TIME_ZONE as the behavior / originally did prior to this change. /  / Account learned how to convert a given datetime object into the timezone of / an account with Account.localtime.
* Added ACCOUNT_DELETION_EXPUNGE_HOURS to settings /  / The lower limit of hours before the account is deleted is now configurable.
* Added account deletion callbacks /  / The new callbacks allow a site developer to customize the behavior of account / deletion entirely.
* Bumped version for next release
* Added AccountDeletion to admin
* Decided to change AccountTimezoneMiddleware to TimezoneMiddleware /  / This change helps unify the naming. Originally it was decided to add the / "Account" prefix, but now realizing it breaks consistency.
* Cleaned up middleware.py
* Cleaned up and simplified account deletion
* Create email address object on account creation /  / When an account is created we need to make sure an email address is created / if asked (default) and User object has one defined. This fixes cases where / accounts are created with email authentication as those accounts are unable / to be logged in to. /  / Fixes #34 — thanks Luke Hatcher for the report.
* Simplified password reset conditions on email /  / This change allows any email address regardless of which state to be used for / password reset. The email sent is harmless as the action of password reset / is non-destructive. /  / This allows a simpler means for those without confirmed emails due to missing / the email or some other reason to reset their account password.
* allow for setting form kwargs in auth views /  / defaults to as before for backwards compatibility, / but easy to override form kwargs by adding / form_kwargs to your site-specific auth views.
* add form prefixes to log in and sign up views /  / adds "login" and "signup" as prefixes to the forms / on the log in and sign up views. this allows for / a custom view that renders both forms without / conflicting field names.
* Respect ACCOUNT_EMAIL_CONFIRMATION_EMAIL when changing email
* Brosner's style suggestions
* Bumped version for next release
* Fixed copy/paste bug in EmailAddress.change
* Bumped version for next release
* Improved account primary email address change /  / When a user changed their primary email address we would simply update the / email address fields. This is problematic because we have no guarantee the new / address is owned by the user. /  / We now update the fields, set the email as unverified and send a confirmation. / If an exception happens during this process we rollback the changes as if the / email never changed.
* Anonymous users don't have an account
* Adds timezone middleware
* Changed email address lookup during authentication /  / When looking up a user account for authentication by email address, we need / to take primary into consideration. /  / If the email address is primary we ignore the verified check (restores / previous behavior after sign up and EMAIL_CONFIRMATION_REQUIRED = False.) /  / If email address is not primary then it must be verified to ensure people / don't hijack other people's email addresses. /  / Thanks Luke Hatcher for discovering this small bug.
* Improved get_*_url when default_redirect is used /  / You can now pass fallback_url to methods which use default_redirect. This / makes customizing the redirect URL simpler when you need data from the / request to build the URL.
* Fixed copy and paste bug with after_login
* Fixed typo in signal name
* Added login signals /  / This commits adds two new signals which are similiar to their sign up / counterparts. user_logged_in and user_login_attempt which are sent as they / are named. /  / Couple of other changes made to make the signals work such as unifying the / interface to get the identifier field for each login form and added / LoginView.after_login.
* Fixed EmailAddressManager.add_email and calling code /  / EmailAddressManager.add_email will not send confirmation if verified is True. / Also, updated SignupView to take advantage of this with some minor clean ups.
* Fixed EmailAuthenticationBackend email lookup /  / When we look up an email address for a user during authentication we must / only look for verified email addresses.
* Added UsernameAuthenticationBackend /  / This change adds a new username backend which does a case-insensitive lookup / on username (Django does case-sensitive.) This commit also unifies the / credential keys to allow email authentication with username fallback. /  / Backwards incompatible if you wrote a custom authentication, overrode / the authenticate method and use LoginEmailForm.
* Notify user when password is changed /  / When a password change occurs we now notify the user by default. This is very / useful for detecting when something bad might be going on for a user. If a / user receives this email when they did not expect they can now talk to the / site owner to get the situation fixed.
* removed ACCOUNT_CONTACT_EMAIL (moved to theme)
* Bumped version
* Fixed user_post_save to run properly
* Added missing receiver import
* Bumped version
* Create accounts on User creation. /  / When a User instance is created we now create an associated Account / object. We make sure that User.save calling code has control over whether / the creation happens. This allows our SignupView to have full control over / the account creation. /  / Fixes #26 — thanks to Douglas Meehan for the report.
* Improved email confirmation control. /  / EmailAddressManager.add_email now accepts confirm kwarg to control whether / it will send a confirmation email. It is turned OFF by default (if you are / calling add_email directly.) /  / Added confirm kwarg to SettingsView.update_email which defaults to the value / of ACCOUNT_EMAIL_CONFIRMATION_EMAIL. /  / This patch fixes #24 which reported a bug in when we display the email / confirmation user message after sign up. Thanks Dave Lowe.
* implemented account deletion
* Removed user check on GET in ConfirmEmailView /  / This was overlooked in 90d8c74f.
* bumped version to represent current state
* updated version
* Removed user check when confirming email address /  / We can't try to be clever and ensure the email address confirmation is / coming from who we expect. This view can be called anonymously due to / ACCOUNT_EMAIL_CONFIRMATION_REQUIRED being True. Fixes #21 and #22.
* updated translations
* added source_file to .tx/config to enable tx push -s
* added admin.py with SignupCode
* changed to use redirect in SignupView.form_valid
* moved middleware into the package
* fixed whitespaces and quotes
* removed create_account signal receiver; User.save side-affect is simply not worth it
* updated file_filter to be correct for app
* added .tx directory
* added English django.po
* added test for SignupView successful post
* made SignupView get test independent from ACCOUNT_OPEN_SIGNUP setting
* reverted SignupView authentication check
* removed unused TemplateView import from views
* fixed SignupView tests
* improved email address handling
* improved SettingsView extensibility
* fixed #18 — added ACCOUNT_REMEMBER_ME_EXPIRY setting
* bump to 1.0b1.dev2 for next release
* fixed #17 — update installation documentation
* removed call to list (not needed)
* changed ACCOUNT_TIMEZONE_CHOICES to ACCOUNT_TIMEZONES to match ACCOUNT_LANGUAGES
* added periods in messages to be consistent
* updated pytz and added some docs regarding its usage
* corrected documentation around ACCOUNT_EMAIL_UNIQUE
* added ACCOUNT_EMAIL_CONFIRMATION_EMAIL to turn off all confirmation emails if desired
* fixed SignupView.form_valid to pass form to create_account
* fixed the remaining password fields to match convention
* updated SignupForm to match password field convention naming
* changed ChangePasswordForm field names to be consistent with new convention
* improved account creation and language value for accounts
* fixed setting name
* fixed SettingsView to check for language before assigning it
* fixed style issue
* fixed SettingsForm to only include language when settings.I18N is turned on
* added email to SignupForm initial data if present on signup code
* added Account.now method
* added form to user_signup signal
* fixed #15 — always override primary email and never add
* double quotes change
* Merge branch 'add-account'
* allow site object to be passed in to send methods
* forcibly remove newlines from subject
* Make language choices display in native language
* Enable SettingsForm to process updates without changing the email address
* Fix use of AppConf
* Drop the get_or_create for a plain create
* Move TIMEZONE_CHOICES to conf
* Add support for timezone/language settings
* improved password reset APIs and some behavior
* changed PASSWORD_CHANGE_REDIRECT_URL default to redirect to itself
* isolated ACCOUNT_OPEN_SIGNUP and signup codes to SignupView.is_open
* added step to installation
* added @login_required decorator to behave similiar to LoginRequiredMixin
* added SettingsView and SettingsForm for handling changes to the user account
* fixed bug where no primary email address is created during signup and cleaned up the code
* cleaned up code style in forms.py
* Corrected reference errors in signup code send email method. /  / Additionally pass current site object instead of domain name to message templates.
* no idea how that "s" sneaked in ;)
* moved view imports in urls.py
* added missing trailing slash
* added missing backticks
* tweaked password related URLs
* cleaned up some whitespace in views.py
* Renamed message key to match other view.
* Corrected password change redirect url.
* Emit password reset confirmation message only if defined in messages dict.
* Renamed password reset message key.
* Added messages dict for change password view.
* added MANIFEST.in
* moved get_user to a better position
* small cleanup
* added signup_url to context of signup invitation
* added PasswordResetKeyView.get_user method to reduce code duplication
* fixed typos and changed position of get_success_url
* changed code style and fixed whitespace
* Merge remote-tracking branch 'binarydud/password_additions' /  / Conflicts: / 	account/forms.py
* Added remaining schema changes for migration from Pinax.
* Corrected form module name in usage example.
* Moved common variable declaration outside try/except block.
* EmailAddress requires user object on creation.
* Added missing method param.
* changes based on feedback from pull request
* added django.contrib.auth dependency
* added FAQ
* Fixed typo.
* added missing import in usage docs
* added a missing import in usage docs
* added doc section to usage for "Customizing the sign up process"
* added missing auth_backends.py file
* added extra depth to TOC
* added usage section on "Allow non-unqiue email addresses"
* added step about user representation to docs
* added SignupForm to no-username step
* added some usage documentation for doing email authentication
* allow kwargs in SignupView.create_user passed through to User
* changed to use exists in SignupForm
* added better support for ACCOUNT_EMAIL_UNIQUE
* added `user_display user` tag
* Merge branch 'master' into password_additions
* adding password reset functionality
* dropped uniqueness on SignupCode.email to allow for new codes
* added more SQL migration
* updated CHANGELOG in docs
* updated docs/conf.py
* started migration guide
* prevent other users from confirming email addresses which do not belong to them
* change password view added
* removed print statement
* fixed ?next= support (only templates handled it)
* added ACCOUNT_CONTACT_EMAIL
* changed open_signup context variable to upper case with ACCOUNT_ prefix
* added account context processor
* if signup code has email attached and it matched given email on signup then ignore any email confirmation
* ACCOUNT_OPEN_SIGNUP should default to True
* implemented signup codes into sign up
* improved SignupCode behavior
* improved SignupCode.create to not be only email based
* we've decided to go directly for a 1.0 once a beta proves stable amoungst our sites
* corrected ordering style of EmailConfirmation model
* changed default ACCOUNT_EMAIL_CONFIRMATION_REQUIRED to False (was temporarily True for testing)
* mark user account active upon confirmation
* separated creation and sending of email confirmations
* changed LogoutView to inherit View directly and use TemplateResponseMixin instead
* implemented ConfirmEmailView and cleans up to supporting bits
* implemented signup with email confirmation
* removed another method using disabled
* removed disabled ability in favour of overriding get/post
* updated README
* added initial incomplete documentation
* added django-appconf 0.5 to install_requires
* moved to setuptools
* added account app; being fresh-started from Pinax thus incomplete
* initial commit of README and setup.py
