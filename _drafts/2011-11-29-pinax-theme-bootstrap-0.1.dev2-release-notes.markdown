---
layout: post
title: "pinax-theme-bootstrap 0.1.dev2 Release Notes"
date: 2011-11-29 19:45:55
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/p/pinax-theme-bootstrap/pinax-theme-bootstrap-0.1.dev2.tar.gz>

This release includes the following:

* update version
* update banner base
* switch to banner base and four column layout
* bump version
* add back django-notification templates
* removing legacy idios css, fixes #7
* removing an extra s
* bump version to 0.1
* show openid register and log in forms when ACCOUNT_USE_OPENID is True
* add a hero_base.html template for usage in start pages
* switch to an include for messages, should be included on all base layout templates
* add a message to site_base.html explaining why it exists
* Make heading h2 to be consistant with account templates
* Pinax does not ship with this css anymore
* Upgrade to work with latest (0.3a1.dev5) notifications
* add blank models
* upgrading to latest bootstrap + jquery
* add template for idios additional info
* properly style non-field form errors, fixes #5
* fixed modal closing in the profile edit success case
* added back close as its styling *is* needed for the X
* fixed modal closing from the X after class name change
* changed close class to not clash with a class that styles differently
* Fix alert message closing behavior
* remove safe filter from field errors / fixes a vector for script injections. thanks to Miguel Araujo for bringing this to our attention.
* revert opened form on log in page
* fade alerts
* use the native alerts code
* update to bootstrap 1.4
* added styled openid error template
* cleaned up openid associate template styling
* cleaned up openid associations template
* bootstrap-styled openid/register
* focus on openid url
* moving openid login to own template
* more consistent openid in login/signup
* use url name for openid register
* removed accidentally copy-pasted code from a while back
* clean up sign up template open id form
* Extending just gave us a new error. Making it blank should fix everything.
* Add a simple site_bas.html. This is a work around to Django issue #17020
* Merge branch 'bootstrap-1.3'
* add styling to log in button
* adding confirm email template
* fixing up openid templates
* adding openid templates
* adding error templates (copied from classic theme)
* adding bootstrap 1.3 assets (css and js plugins)
* fix message closing
* login -> log in
* apologetic commit message, now with actual javascript comments
* add message closing, clean up theme.js order
* adding dropdown to account bar
* added .gitignore
* added brand new modal support with AJAX loading of links and forms within the modal
* javascript-based selection of active nav; no more site_tabs.css
* renaming secondary_nav block to account_bar
* added backdrop and removed fade
* profile edit is now a modal
* add ajax csrf fix
* indent and comment out theme javascript for now
* rename theme javascript base file from pinax.js to theme.js
* added new subnav base template that app bases can use for subnav
* added notification templates
* fixed typo with alert message
* change pagination template to match indentation of the rest of the project
* add a bootstrap formatted pagination template
* initial inclusion of idios templates without modal popover support
* don't mention Pinax in timzone template; just say 'this site'
* some updates to bootstrap css from 1.3-wip including fix for non-anchor text in topbar
* 0.1.dev2
* use local copy of jquery so that I can hack on the plane
* upgrade to latest bootstrap
* added bootstrap js files
* Added messages template tags to work with bootstrap-alerts
* changed load bootstrap_form_filters to load bootstrap_tags
* fixed up packaging
* updated app name in README
* updated account templates to reflect templatetag filename change
* updated README to reflect templatetag filename change
* fixed directory structure snafu and renamed templatetags file
* updated README
* updated manifest
* renamed package
* added gitignore with pyc
* updated setup.py
* password reset should not be on account base
* fixed up forms for login and signup
* implemented form filter for bootstrap and convert account forms over
* more form styling for account
* improved form styling
* added jquery to theme base
* changed no email warning to use alert warning styling
* added note about account subnav
* changed account pages to use columns for subnav
* updated README about site name and secondary nav
* username on secondary nav needs to be an anchor but not sure what it should link to if no profile
* initial implementation of bootstrap theme for pinax
