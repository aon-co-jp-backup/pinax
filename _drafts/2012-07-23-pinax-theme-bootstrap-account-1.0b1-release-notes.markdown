---
layout: post
title: "pinax-theme-bootstrap-account 1.0b1 Release Notes"
date: 2012-07-23 10:00:25
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/p/pinax-theme-bootstrap-account/pinax-theme-bootstrap-account-1.0b1.tar.gz>

This release includes the following:

* Added dist to .gitignore
* Added account delete template
* Prepare for next release
* Fix misspelling
* close the legend tag properly
* use legend instead of page title for log in form /  / using the legend looks better in most cases so it should be the default
* remove legend from log in form /  / fixes unnecessary duplication with page header
* Added password change email notification templates
* added THEME_ACCOUNT_CONTACT_EMAIL in place of relying on d-u-a
* bumped version
* added context processor and setting for controlling admin URL
* changed to new `url` tag from the future
* bump version to reflect current state
* bump version to reflect current state
* removed template not used
* fixed titling of pages
* fixed bug with MANIFEST.in
* added MANIFEST.in
* set version
* added source_file to .tx/config to enable tx push -s
* updated english po
* added transifex and english po
* added .gitignore
* updated context variable in invitation subject
* updated context variable in invitation email
* updated base.html to be functional
* only show "logged in as" label if logged in
* header on log in page
* i18n and fix form markup
* i18n and "logged in as" label
* Modify account base template to extend site_base instead of theme_base
* use form legends when possible
* added password related templates
* added missing account/settings.html template
* added link to account settings from _account_bar.html
* changed invite_user.txt to use new {{ signup_url }} variable
* Added email templates for invite user action (copied from pinax-theme-bootstrap signup_codes).
* fixed login and signup forms to check for is_multipart
* fixed user representation in _account_bar.html
* added updated _account_bar.html
* added version
* initial commit of app and templates
